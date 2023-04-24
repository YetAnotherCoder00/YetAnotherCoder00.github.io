<script lang="ts">

    let transformedcardbool: boolean = false;

</script>

<div>
    <h2>Gehen Sie mit Ihrem Mouse Cursor auf die Karte</h2>
    <div class="body">
        <div class="card" class:transformedcard={transformedcardbool}>

        </div>
        <div class="card" class:transformedcard={transformedcardbool}></div>
        <div class="blurred" class:transformedcard={transformedcardbool} on:mouseenter={() => transformedcardbool = true} on:mouseout={() => {transformedcardbool = false}}>
            Content
        </div>
    </div>
</div>



<style>
    :root {
        --skew1: 20deg;
        --skew2: 0deg;
    }

    .blurred {
        background: rgba(255, 255, 255, 0.1);
        backdrop-filter: blur(5px);
        border-radius: 5%;
        height: 39vh;
        margin-top: 0;
        margin-left: -29vh;
        padding: 2vh;
        width: 30vh;
        transform: skewY(var(--skew2));
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
        transform: skewX(var(--skew1));
        background-size: cover;
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

    .card:nth-child(1) {
        margin-left: 10vh;
        z-index: 1;
    }

    .card:nth-child(2) {
        margin-left: -19vh;
        scale: 1.05;
        backdrop-filter: blur(1vh);
        z-index: 0;
    }

    .transformedcard {
        transform: skewY(0deg);
    }

    .blurred:hover {
        --skew1: 0deg;
        --skew2: 0deg;
    }

</style>