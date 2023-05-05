<svelte:head>
    <title>Qualifikationen</title>
</svelte:head>

<div class="body">
    <h2>Qualifikationen</h2>
    <div class="body2">
        <img src="qualifikationen.png" style="width: 25%">
    </div>
    <br> <br>
    <div class="card-group">
        <h1 class="card">
            Kompetenzen sind Fertigkeiten und Fähigkeiten die es einem ermöglichen komplexe Situationen erfolgreich und effizient zu bewältigen. Dazu gehört z.B. die Handlungskompetenz. <br><br>
        </h1>
        <p class="card">
            Qualifikationen sind Kombinationen aus verschiedenen Kompetenzen, welche für die Bewältigung von Aufgaben von Nöten sind und somit auch von aussen stehenden Stellen gefordert bzw. anerkannt sein können.
        </p>

        <p class="card">
            Reflexion <br> <br>
            Qualifikationen sind wichtig, da man mithilfe von ihnen mehrere Kompetenzen gleichzeitig zusammenfassen kann. Dies hilft z.B. dem Arbeitsgeber, welcher besser 
            bewerten kann, ob der Angestellte zum Job passt.
        </p>
    </div>

    <br> <br>
</div>

<style>

    .body2 {
        display: flex;
        justify-content: space-evenly;
    }

    h2 {
        font-size: 4vh;
        margin: 0;
        padding-top: 10vh;
        padding-bottom: 5vh;
    }

    p {
        font-size: 2vh;
        transition: cubic-bezier(.17, .67, .66, .91) 0.15s;
        pointer-events: none;
        margin: 5vh;
    }
    
    h1 {
        font-size: 3vh;
        margin: 3vh 3vh 0 3vh;
    }

    img {
        justify-self: baseline;
    }

    
    .card-group {
        justify-content: space-evenly;
        flex-direction: row;
        display: flex;
    }

    .card {
        padding: 2vh;
        width: 25vh;
        margin: 1vh;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        transition: cubic-bezier(.17,.67,.66,.91) 0.15s;
        grid-area: center;
        aspect-ratio: 5 / 7;
        font-size: 1.75vh;
    }
</style>