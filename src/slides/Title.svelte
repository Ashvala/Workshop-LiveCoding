<script>
    import { onMount } from 'svelte';
    import Slide from '../lib/Slide.svelte';
    import Code from '../lib/Code.svelte';

    let title;
    onMount(() => {
        let timeout;
        title = new Promise(resolve => {
            timeout = setTimeout(() => resolve('LIVE CODING:an introduction'), 1000);
        });
        () => clearTimeout(timeout);
    });
</script>

<Slide>
    <h2>
        {#await title}
            Wait a sec...
        {:then result}
            {result}
        {/await}
    </h2>
    <h2 class="code_style"> 
        Ash x IJC8 (fka M3RGE C0NFL1CT)
    </h2>
</Slide>
<style> 
    .code_style {
        font-family: 'Fira Code', monospace;
        font-size: 1.5em;
        color: #f8f8f2;
        text-align: center;
    }
</style>
