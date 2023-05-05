

<script lang="ts">

</script>

<svelte:head>
    <title>Home</title>
</svelte:head>

<div class="body">
    <h1>
        Modul 431
    </h1>

    <p>Willkommen auf meiner Seite! Hier werde ich erklären, was wir alles im Modul 431 gemacht haben!</p>
    <p>Doch bevor Sie auf das Menu Icon oben rechts klicken, muss ich erklären, was genau ein Projekt eigentlich ist.</p>
    <h2>Ein Projekt ist ein Vorhaben, das im Wesentlichen durch Einmaligkeit, der Bedingungen in ihrer Gesamtheit gekennzeichnet ist.  Die Eigenschaften, welche ein Projekt haben muss sind: Ein konkretes Ziel, begrenzte Ressourcen, zeitliche Begrenzung, Grösse und Komplexität, Einmaligkeit und Neuartigkeit.</h2>

    <div class="projektmerkmale">
        <div class="merkmal">
            <h2>Konkretes Ziel</h2>
            <p>Es braucht ein konkretes und messbares Ziel. Meist ist dieses Ziel ein zu lösendes Problem. Dafür ist oft eine detaillierte Planung sehr hilfreich.</p>
        </div>
        <div class="merkmal">
            <h2>Begrenzte Ressourcen</h2>
            <p>Bei einem Projekt ist man immer auf gewisse Ressourcen angewiesen, z.B. Personen, Geld oder andere Hilfsmittel. Diese sind nur in beschränktem Masse vorhanden.</p>
        </div>
        <div class="merkmal">
            <h2>Zeitliche Begrenzung</h2>
            <p>In der Regel wird schon zu Beginn eines Projekts ein Zeitpunkt festgelegt, an dem es fertig sein muss. </p>
        </div>
        <div class="merkmal">
            <h2>Grösse und Komplexität</h2>
            <p> Von einem Projekt spricht man erst dann, wenn es gewissermassen umfangreich und komplex ist.</p>
        </div>
        <div class="merkmal">
            <h2>Einmaligkeit und Neuartigkeit</h2>
            <p>Ein Projekt ist immer eine einmalige Sache. Einzelne Elemente eines Projekts können aber trotzdem gleich wie bei anderen sein.</p>
        </div>
    </div>

    <img src="systemtechnik.jpeg" alt="Systemtechnik Bild" style="width: 25%">
</div>

<style>

    .projektmerkmale {
        display: flex;
        flex-direction: row;
        justify-content: center;
        flex-wrap: wrap;
    }

    .merkmal {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex-wrap: wrap;
    }
    h1 {
        font-size: 8vh;
        margin: 0;
        padding: 10vh 0 0 0;
    }

    h2 {
        font-size: 4vh;
        margin: 5vh;
        margin-bottom: 0vh;
    }

    p {
        font-size: 3vh;
    }

</style>