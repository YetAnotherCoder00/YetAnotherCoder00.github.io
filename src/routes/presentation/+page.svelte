<script lang="ts">


    let container: HTMLDivElement;
    let inner: HTMLDivElement;

    let command: string;
    let mouse = { x: 0, y: 0 };

    function handleMousemove(event: MouseEvent) {
        mouse.x = event.clientX;
        mouse.y = event.clientY;

        command = (mouse.x / 10).toString() + "deg " + (mouse.y / 10).toString() + "deg";
        console.log(command);

        inner.style.transform = "rotateY(" + (mouse.x / 100 - window.innerWidth / 205).toString() + "deg) rotateX(" + (-mouse.y / 100 + window.innerHeight / 215).toString() + "deg)";
    }

</script>

<div>
    <h2>Gehen Sie mit Ihrem Mouse Cursor auf die Karte</h2>
    <div class="body">
        <div id="container" bind:this={container}>
            <div id="inner" bind:this={inner} on:mousemove={handleMousemove}>
                Content
            </div>
        </div>
    </div>
</div>

<style>

    h2 {
        font-size: 4vh;
        margin: 0;
        padding-top: 10vh;
        padding-bottom: 5vh;
    }

    .body {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 50vh;
    }

    #container {
        perspective: 100px;
    }

    #inner {
        aspect-ratio: 5 / 7;
        width: 24vh;
        padding: 5vh;
        margin: 5vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
    }

</style>