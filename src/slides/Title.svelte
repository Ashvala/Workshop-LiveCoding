<script>
    // import { onMount } from 'svelte';
    import Slide from '../lib/Slide.svelte';

    // let title;
    // onMount(() => {
    //     let timeout;
    //     title = new Promise(resolve => {
    //         timeout = setTimeout(() => resolve('LIVE CODING:an introduction'), 1000);
    //     });
    //     () => clearTimeout(timeout);
    // });
</script>

<Slide>
    <div class="code">
        <h1 class="hack">
            <!-- {#await title}
                Wait a sec...
            {:then result}
                {result}
            {/await} -->
            LIVE CODING:
        </h1>
        <h2 class="hack">An Introduction</h2>
        <h2> 
            Ash <span class="gray">x</span> IJC
        </h2>
        <small class="gray">(fka M3RGE C0NFL1CT)</small>
    </div>
</Slide>
<style> 
    .code > * {
        font-family: 'Fira Code', monospace;
    }

    .gray {
        color: gray;
    }

    .hack {
        color: #00ef11;
    }
</style>
