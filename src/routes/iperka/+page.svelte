<script lang="ts">

    let cardgroup: HTMLDivElement;
    let one: HTMLDivElement;
    let two: HTMLDivElement;
    let three: HTMLDivElement;

    let showCards: boolean = false;

    function cardanimation() {
        if (!showCards) {
            one.style.marginLeft = "0vh";
            two.style.marginLeft = "4vh";
            three.style.marginLeft = "6vh";
            one.style.rotate = "0deg";
            two.style.rotate = "0deg";
            three.style.rotate = "0deg";
            showCards = true;
        }
        else {
            one.style.marginLeft = "0vh";
            two.style.marginLeft = "-33vh";
            three.style.marginLeft = "-40vh";
            one.style.rotate = "4deg";
            two.style.rotate = "-4deg";
            three.style.rotate = "-8deg";
            showCards = false;
        }
    }

</script>


<svelte:head>
    <title>IPERKA</title>
</svelte:head>


<div class="card-group" id="cardgroup" bind:this={cardgroup}>

    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="card" on:click={cardanimation} bind:this={one}>
        IPERKA Erklärt <br> <br>
        Iperka steht für Informieren, Planen, Entscheiden, Realisieren,
        Kontrollieren und Auswerten. Zuerst informiert man sich über den
        Auftrag, dann schaut man die konkreten Möglichkeiten an,
        danach entscheidet man sich für einen Weg. Im 4. Schritt wird konkret
        geschaut, wie man das Projekt realisiert. Der 5. Schritt besagt, dass
        man das Projekt im Auge behält. Anschliessend wird alles ausgewertet,
        für das nächste Projekt.
    </div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="card" on:click={cardanimation} bind:this={two}>
        Meine Meinung <br> <br>
        Man kann mithilfe des IPERKA Modells Projekte besser managen und auch
        daraus lernen für zukünftige Projekte.
    </div>

    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="card" on:click={cardanimation} bind:this={three}>
        <img src="lightbulb.jpeg" alt="Licht" style="width: 50%">
    </div>

</div>


<style>

    .card {
        padding: 2vh;
        width: 30vh;
        margin: 25vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        transition: cubic-bezier(.17,.67,.66,.91) 0.15s;
        grid-area: center;
        aspect-ratio: 5 / 7;
        font-size: 1.75vh;
    }

    .card-group {
        justify-content: center;
        flex-direction: row;
        display: flex;
    }

    .card:nth-child(1) {
        margin-left: 2vh;
        z-index: 2;
        rotate: 4deg
    }

    .card:nth-child(2) {
        z-index: 1;
        margin-left: -39vh;
        rotate: -4deg;
    }

    .card:nth-child(3) {
        z-index: 0;
        margin-left: -40vh;
        rotate: -8deg;
    }

</style>