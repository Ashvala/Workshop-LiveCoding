<!-- Based on https://www.npmjs.com/package/@strudel.cycles/embed?activeTab=explore -->
<script>
    export let code
</script>
<iframe width={600} height={400} src={`https://strudel.tidalcycles.org/#${encodeURIComponent(btoa(code))}`} title="Strudel"></iframe>
