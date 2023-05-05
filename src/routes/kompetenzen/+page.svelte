<svelte:head>
    <title>Kompetenzen</title>
</svelte:head>

<div class="body">
    <h2>Kompetenzen</h2>
    <!-- svelte-ignore a11y-missing-attribute -->
    <div class="body2">
        <img src="kompetenzen.png" style="width: 25%">
        <img src="handlungskompetenzen.png" style="width: 25%">
    </div>
    <h1>
        Kompetenzen sind Fertigkeiten und Fähigkeiten die es einem ermöglichen komplexe Situationen erfolgreich und effizient zu bewältigen. Dazu gehört z.B. die Handlungskompetenz. <br><br>
    </h1>
    <div class="card-group">
        <p class="card">
            Zu den Sozialkompetenzen gehören Fertigkeiten und Fähigkeiten, die es ermöglichen, sich im Umgang mit Mitmenschen angemessen zu verhalten. <br> <br>

            Beispiele: Teamfähigkeit, Hilfsbereitschaft, Empathie, Gute Umgangsformen<br> <br>
        </p>
        <p class="card">
            Als Sachkompetenz ergibt sich aus den Sachkenntnissen, also dem Wissen, und Fertigkeiten, die für die Bewältigung bestimmter fachlicher Aufgaben notwendig sind. <br> <br>

            Beispiele: Mathematik-, Physik-, Englisch oder Wirtschaftskenntnisse<br> <br>
        </p>
        <p class="card">
            Die Methodenkompetenz umfasst Fertigkeiten, Kenntnisse und vor allem die Beherrschung und Anwendung verschiedener allgemein gebräuchlicher, zum Teil auch spezifischer Arbeitsmethoden und Techniken.  <br> <br>

            Beispiele: Arbeitstechnik, Projektmanagement, Kreativitätstechnik, Präsentationstechnik<br> <br>
        </p>
        <p class="card">
            Die Selbstkompetenz beschreibt die verhaltensrelevanten Persönlichkeitsmerkmale, die den Umgang mit der eigenen Person betreffen.<br> <br>

            Beispiele: Selbstbewusstsein, Konzentrationsfähigkeit, Kreativität, Emotionale Kompetenz
        </p>
        
        <p class="card">
            Reflexion <br> <br>
            Meiner Meinung nach ist es wichtig, dass man weiss, was Kompetenzen sind und dass es verschiedene Arten von Kompetenzen gibt. Dadurch kann man sogar,
            falls man nicht so stark in der einten Kompetenz, mit einer anderen Kompetenz dies kompensieren.
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
        flex-wrap: wrap;
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