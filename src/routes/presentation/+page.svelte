<script lang="ts">


    let container: HTMLDivElement;
    let inner: HTMLDivElement;

    let container2: HTMLDivElement;
    let inner2: HTMLDivElement;

    let mouse = { x: 0, y: 0 };

    function handleMousemove(event: MouseEvent) {
        mouse.x = event.clientX;
        mouse.y = event.clientY;

        inner.style.transform = "rotateY(" + (mouse.x / 100 - window.innerWidth / 250).toString() + "deg) rotateX(" + (-mouse.y / 100 + window.innerHeight / 215).toString() + "deg)";
    }

    function handleMousemove2(event: MouseEvent) {
        mouse.x = event.clientX;
        mouse.y = event.clientY;

        inner2.style.transform = "rotateY(" + (mouse.x / 100 - window.innerWidth / 175).toString() + "deg) rotateX(" + (-mouse.y / 100 + window.innerHeight / 215).toString() + "deg)";
    }
</script>


<svelte:head>
    <title>Präsentationstechniken</title>
</svelte:head>

<div>
    <h2>Gehen Sie mit Ihrem Mouse Cursor auf die Karte</h2>
    <div class="body">
        <div id="container" bind:this={container}>
            <div id="inner" bind:this={inner} on:mousemove={handleMousemove}>
                Mithilfe von Präsentationstechniken kann man bessere Präsentationen halten,
                damit man seine Idee besser verkaufen oder besser erklären kann. Dies kann
                man mithilfe einer sicheren Körperhaltung und ohne Füllwörter zu benutzen, erreichen.
            </div>
        </div>
        <div id="container2" bind:this={container2}>
            <div id="inner2" bind:this={inner2} on:mousemove={handleMousemove2}>
                Präsentationstechniken sind für mich sehr wichtig, weil man sehr vieles präsentieren muss. Sie sind für mich auch wichtig, da man mir schon früh gelehrt hatte, wie wichtig eine
                gute Präsentation ist. Für mich bedeutet dies auch zum Beispiel grundsätzlich kein Text oder sehr wenig Text auf den Folien zu haben.
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
        font-size: 1.75vh;
    }

    #container2 {
        perspective: 100px;
    }

    #inner2 {
        aspect-ratio: 5 / 7;
        width: 24vh;
        padding: 5vh;
        margin: 5vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        font-size: 1.75vh;
    }

</style>