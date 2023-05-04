<script lang="ts">

    let card1transformed: boolean = false;
    let card2transformed: boolean = false;

</script>

<svelte:head>
    <title>Projektmanagement</title>
</svelte:head>

<div>
    <h2>Gehen Sie mit Ihrem Mouse Cursor auf die Karte</h2>
    <div class="body">
        <div class="card" class:transformedcard={card1transformed}>

        </div>
        <!-- svelte-ignore a11y-mouse-events-have-key-events -->
        <div class="blurred" class:transformedcard={card1transformed} on:mouseenter={() => card1transformed = true} on:mouseout={() => {card1transformed = false}}>
            Beschreibung <br>
            Hier geht es darum, wie man mit einem Projekt umgeht und welche Methoden es dafür gibt.
            Es gibt zum Beispiel das Wasserfallmodell, in welchem die oberen / vorherigen Phasen für die
            nächste vorgegeben sein müssen, SCRUM, in welchem Sprints zentral sind und viele weitere.
        </div>

        <div class="card" class:transformedcard={card2transformed}>

        </div>
        <!-- svelte-ignore a11y-mouse-events-have-key-events -->
        <div class="blurred" class:transformedcard={card2transformed} on:mouseenter={() => card2transformed = true} on:mouseout={() => {card2transformed = false}}>
            Meine Meinung <br>
            Meiner Meinung nach ist es wichtig zu wisesen, was für Projektmanagement- methoden existieren.
            Es ist aber vor allem wichtig für den Projektleiter, damit er weiss, wie man mit einem Team 
            arbeiten sollte.
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

    @media (max-width: 689px) {
        /* 
        Todo: Insert the body with display flex here and make it change based on the device width
        */

        
        .body {
            display: flex;
            align-items: center;
            flex-direction: column;
            min-height: 50vh;
        }

        .blurred {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(5px);
            border-radius: 5%;
            height: 39vh;
            margin-top: -48vh;
            padding: 2vh;
            font-size: 2.5vh;
            width: 200px;
            z-index: 2;
            margin-bottom: 10vh;
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
            margin-left: 6vw;

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
        
    }

    @media (min-width: 690px){
        .body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 50vh;
        }
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
    }

    

    .transformedcard {
        transform: skewY(0deg);
    }

</style>