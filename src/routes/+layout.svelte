<script lang="ts">

    import { fade } from 'svelte/transition';
    let menu: boolean = false;

</script>

{#if menu}
    <div class="body2" in:fade={{duration: 300, delay: 300}} out:fade={{duration: 300, delay: 0}}>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <i class="fa-solid fa-x fa-2xl" style="top: 20px; right: 10px; position: absolute; z-index: 12;" on:click={() => {menu = false}} transition:fade></i>
        <div style="display: flex; justify-content: center; align-items: center; height: 100vh; flex-direction: column; line-height: 1.6 ">
            <a href="/" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Home</a> <br> <br>
            <a href="/kompetenzen" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Kompetenzen</a> <br> <br>
            <a href="/qualifikationen" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Qualifikationen</a> <br> <br>
            <a href="/eportfolio" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">E-Portfolio</a> <br> <br>
            <a href="/creativitytechniques" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Kreativitätstechniken</a> <br> <br>
            <a href="/iperka" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Vollständige Handlung mit IPERKA</a> <br> <br>
            <a href="/presentation" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Präsentationstechniken</a> <br> <br>
            <a href="/projectmanagement" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Projektmanagement</a> <br> <br>
            <a href="/gesamtreflexion" on:click={() => {menu = false}} data-sveltekit-preload-code="eager" data-sveltekit-preload-data="hover">Gesamtreflexion</a>
        </div>
    </div>
{:else}
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="body" in:fade={{duration: 300, delay: 300}} out:fade={{duration: 300, delay: 0}}>
        <i class="fa-solid fa-bars fa-2xl" style="top: 20px; right: 10px; position: absolute; z-index: 12;" on:click={() => {menu = true}} transition:fade></i>
        <slot />
    </div>
{/if}


<style>

    @media (max-width: 679px) {
        .body {
            align-items: center;
            text-align: center;
            align-content: center;
            background: linear-gradient(#e66465, #9198e5, #e66465) repeat;
            user-select: none;
            min-height: 100%;
            height: auto;
            margin: 0;
            top: 0;
        }
        .body2 {
            align-items: center;
            text-align: center;
            align-content: center;
            background: linear-gradient(#e66465, #9198e5, #e66465) repeat;
            user-select: none;
            min-height: 100%;
            height: auto;
            margin: 0;
            top: 0;
        }
    }

    @media (min-width: 680px){
        .body {
            align-items: center;
            text-align: center;
            align-content: center;
            background: linear-gradient(#e66465, #9198e5) no-repeat;
            user-select: none;
            min-height: 100%;
            height: auto;
            margin: 0;
            top: 0;
        }
        .body2 {
            align-items: center;
            text-align: center;
            align-content: center;
            background: linear-gradient(#e66465, #9198e5) no-repeat;
            user-select: none;
            min-height: 100%;
            height: auto;
            margin: 0;
            top: 0;
        }
    }

    a {
        font-size: 4vh;
        color: black;
        display: inline-block;
        padding-bottom:2px;
        background-image: linear-gradient(#000000, #000000);
        background-position: 0 100%; /*OR bottom left*/
        background-size: 0 2px;
        background-repeat: no-repeat;
        text-decoration: none;
        transition:
                background-size 0.3s,
                background-position 0s 0.3s; /*change after the size immediately*/
    }

    a:hover {

        background-position: 100% 100%; /*OR bottom right*/
        background-size: 100% 2px;
    }
</style>