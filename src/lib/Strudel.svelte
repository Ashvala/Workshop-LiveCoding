<!-- Based on https://www.npmjs.com/package/@strudel.cycles/embed?activeTab=explore -->
<script>
    let data
</script>
<span bind:this={data} style="display: none"><slot /></span>
{#if data}
    <iframe width={600} height={400} src={`https://strudel.tidalcycles.org/#${encodeURIComponent(btoa(data?.innerHTML))}`} title="Strudel"></iframe>
{/if}
