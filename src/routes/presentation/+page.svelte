<script lang="ts">
  import { update_await_block_branch } from "svelte/internal";


    let container: HTMLDivElement;
    let inner: HTMLDivElement;

    let mouse = { x: 0, y: 0 };

    function handleMousemove(event: MouseEvent) {
        mouse.x = event.clientX;
        mouse.y = event.clientY;

        inner.style.perspective = "10px";
    }

</script>

<div class="body">
    <div id="container" bind:this={container}>
        <div id="inner" bind:this={inner} on:mousemove={handleMousemove}>
            {mouse.x}, {mouse.y}
        </div>
    </div>
</div>

<style>

    .body {
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
    }

    #container {
        perspective: 100px;
    }

    #inner {
        width: 20em;
        height: 18em;
        background-color: white;
    }

</style>