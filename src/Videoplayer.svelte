<script>
    import Navbar from './Navbar.svelte';

    export let poster;
    export let src;

    let videoContainer
    let paused = true;
    let time = 0;
    let duration;

    let showControls = true;
    let showControlsTimeout;
    let fullscreenState = false;

    function handleMouseMove(e) {
        clearTimeout(showControlsTimeout);
        showControlsTimeout = setTimeout(() => showControls = false, 2500);
        showControls = true;

        if(!(e.buttons & 1)) return; // Verificando se o botão está sendo segurado
        if(!duration) return; // Se o vídeo não tiver sido carregado, não será possivel reproduzir o vídeo

        const {left, right} = this.getBoundingClientRect();
        time = duration * (e.clientX - left) / (right - left);
    }
    
    function handleProgressBar(e){
        if(!(e.buttons & 1)) return; // Verificando se o botão está sendo segurado
        if(!duration) return; // Se o vídeo não tiver sido carregado, não será possivel reproduzir o vídeo

        const {left, right} = this.getBoundingClientRect();
        time = duration * (e.clientX - left) / (right - left);
    }

    function handleMouseDown(e){

        function cancel(){
            e.target.removeEventListener('mouseup', handleMouseUp);
        }

        function handleMouseUp(){
            if(paused) e.target.play();
            else e.target.pause();
            cancel();
        }

        e.target.addEventListener('mouseup', handleMouseUp);
        setTimeout(cancel, 200);
    }

    function format(seconds) {
        if(isNaN(seconds)) return "...";

        const minutes = Math.floor(seconds / 60);
        const hours = Math.floor(minutes / 60);
        seconds = Math.floor(seconds % 60);

        const stringSeconds = seconds > 9 ? seconds : `0${seconds}`

        if(hours) return `${hours}:${minutes}:${stringSeconds}`;
        else return `${minutes}:${stringSeconds}`;
    }

    function handlePlayPause(e){
        paused = !paused;
    }

    function handleClickFullscreen() {
        if(!fullscreenState) {
            videoContainer.requestFullscreen();
            fullscreenState = true
        }

        else {
            document.exitFullscreen();
            fullscreenState = false
        }
    }
</script>

<section>
    <Navbar/>
    <div class="container">
        <div class="c-video" bind:this={videoContainer}>
            <video
            poster="https://sveltejs.github.io/assets/caminandes-llamigos.jpg"
	        src="https://sveltejs.github.io/assets/caminandes-llamigos.mp4"
            bind:paused
            bind:duration
            bind:currentTime={time}
            on:mousedown={handleMouseDown}
            on:mousemove={handleMouseMove}
            ></video>
            <div class="controls" style="opacity: {duration && showControls ? 1 : 0}">
                
                <progress value="{(time / duration) || 0}" 
                on:mousemove={handleProgressBar}
                />

                <div class="buttons">
                    <div>
                        <button id="btn-play" on:click={handlePlayPause}>
                        {#if !paused}
                            <i class="material-icons">pause</i>
                        {:else}
                            <i class="material-icons">play_arrow</i>
                        {/if}
                        </button>
                        <span class="time">{format(time)} / {format(duration)}</span>
                    </div>
                    <div>
                        <span class="time"></span>
                        <button id="btn-options"><i class="material-icons">settings</i></button>
                        <button id="btn-fullscreen"  
                        on:click={handleClickFullscreen}>
                            <i class="material-icons">fullscreen</i>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </div>
</section>

<style>

    * {
        margin: 0;
        padding: 0;
    }

    progress {
        display: block;
        width: 100%;
        height: 10px;
        opacity: 0.6;
        -webkit-appearance: none;
		appearance: none;
    }

    video {
        width: 100%;
    }

    progress::-webkit-progress-bar {
		background-color: black;
	}

	progress::-webkit-progress-value {
		background-color: red;
	}

    .container {
        background-color: rgba(0, 0, 0, 0.849);
        display: flex;
        justify-content: center;
    }

    .c-video {
        position: relative;
    }

    .controls {
        background-color: rgba(117, 117, 117, 0.6);
        display: flex;
        display: -ms-flexbox;
        display: -webkit-flex;
        flex-direction: column;

        position: absolute;
        bottom: 0;
        width: 100%;

        transition: opacity 0.2s;
        -webkit-transition: opacity 0.2s;
        -moz-transition: opacity 0.2s;
        -o-transition: opacity 0.2s;
    }

    .buttons {
        display: flex;
        display: -ms-flexbox;
        display: -webkit-flex;

        justify-content: space-between;
    }

    .buttons button {
        color: aliceblue;
        background: none;
        border: 0;
        outline: 0;
        cursor: pointer;
        margin: 0;
        padding: 5px;
    }

    .buttons button:focus {
        outline: 0;
        color: rgb(255, 107, 107);
    }

    .time {
        color: white;
        padding: 5px;
        height: 100%;
    }

    #btn-fullscreen:focus {
        color: white;
    }

</style>