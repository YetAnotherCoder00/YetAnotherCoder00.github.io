

<script lang="ts">
    import { scale } from 'svelte/transition';

    let enlarged1: boolean = false;
    let enlarged2: boolean = false;
    let enlarged3: boolean = false;
    let enlarged4: boolean = false;
    let enlarged5: boolean = false;

    function enlarged1toggle(){
        if (enlarged1) enlarged1 = false;
        else if (!enlarged1) enlarged1 = true;
    }

    function enlarged2toggle(){
        if (enlarged2) enlarged2 = false;
        else if (!enlarged2) enlarged2 = true;
    }

    function enlarged3toggle(){
        if (enlarged3) enlarged3 = false;
        else if (!enlarged3) enlarged3 = true;
    }

    function enlarged4toggle(){
        if (enlarged4) enlarged4 = false;
        else if (!enlarged4) enlarged4 = true;
    }

    function enlarged5toggle(){
        enlarged5 = !enlarged5
    }


</script>


<svelte:head>
    <title>Kreativitätsmethode</title>
</svelte:head>

<div class="body">

    <h2>Kreativitätsmethoden<br><br></h2>

    <!-- svelte-ignore a11y-mouse-events-have-key-events -->
    <div class="card-group">

        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="card" id="card1" class:bigCard1="{enlarged1 === true}" on:click={enlarged1toggle} on:mouseout={() => enlarged1 = false}>
            {#if !enlarged1}
                <p id="title1" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Die Walt Disney Methode
                </p>
            {:else}
                <p id="text1" style="font-size: 1.25vh; user-select: none;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Bei dieser Methode hat man vier Stühle. Auf jedem Stuhl sitzt eine Person. Jede Person nimmt eine Rolle ein: Neutral, Kritisch, Realistisch und Träumerisch. <br>
                    Man bringt immer die Perspektive der Person, auf dessen Stuhl man sitzt. Danach wird rotiert. <br>
                    Bei der neutralen Person wird dann zusammengefasst. Dann geht es so lange im Kreis, bis alle Personen damit einverstanden sind und man ist fertig.
                </p>
            {/if}
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="card" id="card2" class:bigCard2="{enlarged2 === true}" on:click={enlarged2toggle} on:mouseout={() => enlarged2 = false}>
            {#if !enlarged2}
                <p id="title2" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Brainstorming
                </p>
            {:else}
                <p id="text2" style="font-size: 1.25vh; user-select: none;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Beim Brainstorming schreiben alle Teilnehmer alle ihre Gedanken, die sie zu einem Thema haben auf ein Blatt, Whiteboard, oder ein anderes geeignetes Medium. <br> <br>
                    Das Ziel dabei ist es, so viele Ideen zu einem Thema zu generieren, wie möglich. Mit Brainstorming meint man das schnelle und ungefilterte Sammeln von Ideen.
                </p>
            {/if}
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="card" id="card3" class:bigCard3="{enlarged3 === true}" on:click={enlarged3toggle} on:mouseout={() => enlarged3 = false}>
            {#if !enlarged3}
                <p id="title3" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Mind-Maps
                </p>
            {:else}
                <p id="text3" style="font-size: 1.25vh; user-select: none;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Bei Mind-Maps will man wie beim Brainstorming so viele verschiedene Ideen sammeln, wie möglich. Diese werden jedoch bei Mind-Maps in strukturierter Form dargestellt. <br><br>
                    Die Begriffe in einer Mind-Map werden gruppiert und durch Blasen getrennt, welche mit Strichen verbundeen sind, um die Assotiationen zwischen verschiedenen Idee-Gruppen festzuhalten. <br><br>
                    Man kann bei Mind-Maps ablesen, wie bestimmte begriffe zusammenhängen. Das kann auch beim überlegen neuer Ideen helfen.
                </p>
            {/if}
        </div>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="card" id="card4" class:bigCard4="{enlarged4 === true}" on:click={enlarged4toggle} on:mouseout={() => enlarged4 = false}>
            {#if !enlarged4}
                <p id="title4" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Die Kuchen Methode
                </p>
            {:else}
                <p id="text4" style="font-size: 1.15vh; user-select: none; line-height: 1.15vh;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 160}}">
                    Wenn man die Kuchen Methode anwendet, geht man beim Überlegen so vor, wie beim Kuchen-Backen:
                    <br><br>
                    Die Zutaten sammeln:
                    Bei diesem schritt macht man ein Brainstorming und schreibt alle Ideen (Zutaten) auf.
                    <br><br>
                    Ein Teig daraus machen:
                    Hier macht man Gruppen aus den gesammelten ideen. Das kann man zum beispiel mit verschiedenen Farben machen.
                    <br><br>
                    Den Teig ruhen lassen:
                    In dieser Phase macht man etwas komplett anderes wie zum beispiel Sport und lässt dabei das Unterbewusstsein an den Ideen arbeiten.
                    <br><br>
                    Den Teig backen:
                    Zu letzt setzt man sich noch mal an die grupierten Ideen, sortiert die nicht so guten aus und fasst die guten zusammen, bis man mit dem Ergebnis zufrieden ist.
                </p>
            {/if}
        </div>

        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="card" id="card5" class:bigCard5="{enlarged5 === true}" on:click={enlarged5toggle} on:mouseout={() => enlarged5 = false}>
            {#if !enlarged5}
                <p id="title5" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Reflexion
                </p>
            {:else}
                <p id="text5" style="font-size: 1.25vh; user-select: none; line-height: 1.25vh;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Meiner Meinung nach sind diese Methoden noch nützlich, sogar um Progleme zu lösen. Man kann damit allgemein Ideen finden, egal für was und dadurch eignen sich diese Methoden auch für andere
                    Dinge.
                </p>
            {/if}
        </div>

    </div>

    <img src="lightbulb.jpeg" alt="Licht" style="width: 25%">

</div>

<style>

    :root {
        --index1: 1;
        --index2: 2;
        --index3: 3;
        --index4: 4;
        --index5: 5;
    }

    h2 {
        font-size: 4vh;
    }

    p {
        font-size: 2vh;
        transition: cubic-bezier(.17, .67, .66, .91) 0.15s;
        pointer-events: none;
        padding: 0vh;
    }

    .card {
        padding: 2vh;
        width: 24vh;
        margin: 5vh 5vh 5vh 0;
        color: white;
        border-radius: 5%;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        transition: cubic-bezier(.17,.67,.66,.91) 0.15s;
        grid-area: center;
        aspect-ratio: 5 / 7;
    }
    @media (min-width: 680px){

        .card-group{
            justify-content: center;
            flex-direction: row;
            display: flex;
        }
        .card:nth-child(1) {
            z-index: var(--index1);
            margin-left: 0;
            margin-right: 0;

        }

        .card:nth-child(2) {
            z-index: var(--index2);
            margin-left: -2vh;
            margin-right: 0;
        }

        .card:nth-child(3) {
            z-index: var(--index3);
            margin-left: -2vh;
            margin-right: 0;
        }

        .card:nth-child(4) {
            z-index: var(--index4);
            margin-left: -2vh;
            margin-right: 0;
        }

        
        .card:nth-child(5) {
            z-index: var(--index5);
            margin-left: -2vh;
            margin-right: 0;
        }

        

        .card:hover {
            width: 24vh;
            rotate: 5deg;

        }

        .bigCard1 {
            --index1: 10;
            scale: 1.8;
        }

        .bigCard2 {
            --index2: 10;
            scale: 1.8;
        }

        .bigCard3 {
            --index3: 10;
            scale: 1.8;
        }

        .bigCard4 {
            --index4: 10;
            scale: 1.8;
        }

        .bigCard5{
            --index5: 10;
            scale: 1.8;
        }
    }
    @media (max-width: 679px){

        .card-group{
            justify-content: center;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
        }
        .card:nth-child(1) {
            z-index: var(--index1);
            margin: 2vh auto 2vh auto;

        }

        .card:nth-child(2) {
            z-index: var(--index2);
            margin: 2vh auto 2vh auto;
        }

        .card:nth-child(3) {
            z-index: var(--index3);
            margin: 2vh auto 2vh auto;

        }

        .card:nth-child(4) {
            z-index: var(--index4);
            margin: 2vh auto 2vh auto;
        }

        .card:nth-child(5) {
            z-index: var(--index5);
            margin: 2vh auto 10vh auto;
        }

        .bigCard1 {
            --index1: 10;
            scale: 1.6;
        }

        .bigCard2 {
            --index2: 10;
            scale: 1.6;
        }

        .bigCard3 {
            --index3: 10;
            scale: 1.6;
        }

        .bigCard4 {
            --index4: 10;
            scale: 1.6;
        }
        
        .bigCard5{
            --index5: 10;
            scale: 1.8;
        }
    }



    


</style>