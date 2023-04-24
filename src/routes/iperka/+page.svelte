<script lang="ts">

    let cardgroup: HTMLDivElement;
    let one: HTMLDivElement;
    let two: HTMLDivElement;

    let showCards: boolean = false;

    function cardanimation() {
        if (!showCards) {
            one.style.marginLeft = "0vh";
            two.style.marginLeft = "4vh";
            one.style.rotate = "0deg";
            two.style.rotate = "0deg";
            showCards = true;
        }
        else {
            one.style.marginLeft = "0vh";
            two.style.marginLeft = "-33vh";
            one.style.rotate = "4deg";
            two.style.rotate = "-4deg";
            showCards = false;
        }
    }

</script>


<div class="card-group" id="cardgroup" bind:this={cardgroup}>

    <div class="card" on:click={cardanimation} bind:this={one}>
        test1
    </div>
    <div class="card" on:click={cardanimation} bind:this={two}>
        test2
    </div>

</div>


<style>

    .card {
        padding: 2vh;
        width: 24vh;
        margin: 25vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        transition: cubic-bezier(.17,.67,.66,.91) 0.15s;
        grid-area: center;
        aspect-ratio: 5 / 7;
    }

    .card-group {
        justify-content: center;
        flex-direction: row;
        display: flex;
    }

    .card:nth-child(1) {
        margin-left: 0;
        z-index: 2;
        rotate: 4deg
    }

    .card:nth-child(2) {
        z-index: 1;
        margin-left: -33vh;
        rotate: -4deg;
    }

</style>