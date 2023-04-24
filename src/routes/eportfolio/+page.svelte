<script lang="ts">

    let one = document.getElementById("one");
    let two = document.getElementById("two");

    function circleLeft() {
        one.style.zIndex = "2";
    }

    function circleRight() {
        console.log("right");
    }

</script>

<div class="body">
    <h2>E-Portfolio</h2>
    <div class="card-group">
        <i class="fa-solid fa-circle-arrow-left fa-2xl" on:click={circleLeft}></i>
        <div class="card" id="two"> <!-- this comes first -->
            Description of the e portfolio
        </div>
        
        <div class="card" id="two">
            My own experiences with it
        </div>
        <i class="fa-solid fa-circle-arrow-right fa-2xl" on:click={circleRight}></i>
    </div>
</div>


<style>

    
    h2 {
        font-size: 4vh;
        margin-top: 0;
        padding-top: 10vh;
    }

    i {
        align-self: center;
        margin: 10vh;
    }

    .card {
        padding: 2vh;
        width: 24vh;
        margin: 5vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        transition: cubic-bezier(.17,.67,.66,.91) 0.15s;
        grid-area: center;
        aspect-ratio: 5 / 7;
    }

    .card-group{
        justify-content: center;
        flex-direction: row;
        display: flex;
    }

    .card:nth-child(2) {
        margin-left: 0;
        margin-right: 0;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        z-index: 5;

    }

    .card:nth-child(3) {
        color: black;
        margin-left: -20vh;
        background: linear-gradient(to right, rgb(255, 255, 255), rgb(126, 126, 126));
        margin-right: 0;
        z-index: 4;
    }

</style>