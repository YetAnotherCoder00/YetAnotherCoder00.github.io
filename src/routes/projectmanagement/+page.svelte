<script lang="ts">

    let card1transformed: boolean = false;
    let card2transformed: boolean = false;

</script>

<div>
    <h2>Gehen Sie mit Ihrem Mouse Cursor auf die Karte</h2>
    <div class="body">
        <div class="card" class:transformedcard={card1transformed}>

        </div>
        <div class="blurred" class:transformedcard={card1transformed} on:mouseenter={() => card1transformed = true} on:mouseout={() => {card1transformed = false}}>
            Beschreibung
        </div>

        <div class="card" class:transformedcard={card2transformed}>

        </div>
        <div class="blurred" class:transformedcard={card2transformed} on:mouseenter={() => card2transformed = true} on:mouseout={() => {card2transformed = false}}>
            Content
        </div>
    </div>
</div>



<style>

    .blurred {
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(5px);
        border-radius: 5%;
        height: 39vh;
        margin-top: 0;
        margin-left: -29vh;
        padding: 2vh;
        font-size: 2.5vh;
        width: 30vh;
        z-index: 2;
    }

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

    .card {
        padding: 2vh;
        width: 10vh;
        margin: 5vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, darkorange, darkred);
        transition: 0.5s;
        grid-area: center;
        height: 40vh;
        margin-left: 12vh;
        transform: skewX(20deg);
        background-size: cover;
        scale: 1.1;
    }

    .card::after {
        width: 100%;
        height: 100%;
        border-radius: 50px;
        position: absolute;
        top: 0;
        left: 0;
        z-index: -1;
        content: '';
        background: inherit;
        filter: blur(20px);
        transform: scale(1.05);
        opacity: 0.8;
        transition: 500ms all ease-in-out 0ms;
    }

    .transformedcard {
        transform: skewY(0deg);
    }

</style>