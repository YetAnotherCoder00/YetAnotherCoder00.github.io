<script lang="ts">
    import { scale } from 'svelte/transition';

    let one: HTMLDivElement;
    let two: HTMLDivElement;

    let showOne: boolean = true;

    let enlarged1: boolean = false;
    let enlarged2: boolean = false;




    function circleLeft() {
        if (showOne) {
            one.style.marginLeft = "-22vh";
            two.style.marginLeft = "2vh";
            setTimeout(() => {
                one.style.zIndex = "1";
                two.style.zIndex = "2";
                one.style.marginLeft = "0";
                two.style.marginLeft = "-20vh";
            }, 150)
            showOne = false;
        }
    }

    function circleRight() {
        if (!showOne) {
            one.style.marginLeft = "-22vh";
            two.style.marginLeft = "2vh"
            setTimeout(() => {
                one.style.zIndex = "2";
                two.style.zIndex = "1";
                one.style.marginLeft = "0";
                two.style.marginLeft = "-20vh";
            }, 150)
            showOne = true;
        }
    }

    function enlarged1toggle(){
        if (showOne){
            if (enlarged1) enlarged1 = false;
            else if (!enlarged1) enlarged1 = true;
        }
    }

    function enlarged2toggle(){
        if (!showOne){
            if (enlarged2) enlarged2 = false;
            else if (!enlarged2) enlarged2 = true;
        }
    }

</script>


<svelte:head>
    <title>E-Portfolio</title>
</svelte:head>

<div class="body">
    <h2>E-Portfolio</h2>
    <div class="card-group">
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-mouse-events-have-key-events -->
        <div class="card" id="one" class:bigCard1={enlarged1} bind:this={one} on:click={() => {enlarged1toggle()}} on:mouseout={() => enlarged1 = false}> <!-- this comes first -->
            {#if !enlarged1}
                <p id="title1" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Beschreibung
                </p>
            {:else}
                <p id="text1" style="font-size: 1.5vh; user-select: none;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                        Ein ePortfolio (elektronisches Portfolio) ist eine digitale Sammlung von Dokumenten, die von einer Person erstellt und gespeichert werden, 
                        um ihre Leistungen, Fähigkeiten, Erfahrungen, Ziele und Fortschritte im Laufe der Zeit zu dokumentieren und zu reflektieren. 
                        Es kann als persönliches Archiv oder als Mittel zur Demonstration von Kompetenzen und Erfahrungen verwendet werden.
                </p>
            {/if}
            
            <p>
                
            </p>
        </div>
        
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-mouse-events-have-key-events -->
        <div class="card" class:bigCard1={enlarged2} id="two" bind:this={two} on:click={() => {enlarged2toggle()}} on:mouseout={() => enlarged2 = false}>
            {#if !enlarged2}
                <p id="title1" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Reflexion
                </p>
            {:else}
                <p id="text1" style="font-size: 1.5vh; user-select: none;" out:scale="{{duration: 150}}" in:scale="{{duration: 150, delay: 150}}">
                    Ich finde es grundsätzlich eine gute Idee, da man damit all seine Fähigkeiten und Projekte zusammen zu fassen. Es macht auch das Leben der Arbeitsgeber einfacher und
                    man kann somit schnell nachschauen, ob jemand für den Job geeignet ist.
                </p>
            {/if}
        </div>
    </div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <i class="fa-solid fa-circle-arrow-left fa-2xl" on:click={circleLeft}></i>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <i class="fa-solid fa-circle-arrow-right fa-2xl" on:click={circleRight}></i>
</div>


<style>

    :root {
        --index1: 1;
        --index2: 2;
    }
    
    h2 {
        font-size: 4vh;
        margin-top: 0;
        padding-top: 10vh;
    }

    
    i {
            align-self: center;
            margin: 7vh;
        }

    p {
        font-size: 2vh;
        transition: cubic-bezier(.17, .67, .66, .91) 0.15s;
        pointer-events: none;
    }


    @media (min-width: 680px){
        .bigCard1 {
            --index1: 10;
            scale: 1.8;
        }
    }
    @media (max-width: 679px){

        .bigCard1 {
            --index1: 10;
            scale: 1.6;
        }
    }

    .card {
        padding: 2vh;
        width: 24vh;
        min-width: 24vh;
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

    .card:nth-child(1) {
        margin-left: 0;
        margin-right: 0;
        background: linear-gradient(to right, rgb(78, 78, 78), black);
        z-index: 5;

        rotate: -4deg;

    }

    .card:nth-child(2) {
        color: black;
        margin-left: -20vh;
        background: linear-gradient(to right, rgb(255, 255, 255), rgb(126, 126, 126));
        margin-right: 0;
        z-index: 4;
        rotate: 4deg;
    }

</style>