<!-- Based on https://www.npmjs.com/package/@strudel.cycles/embed?activeTab=explore -->
<script>
    export let code
    let height = Math.min(45 + (code.trim().split("\n").length + 1) * 25, 500)
</script>
<iframe style="margin: auto" width={600} height={height} src={`https://strudel.tidalcycles.org/#${encodeURIComponent(btoa(code.trim()))}`} title="Strudel"></iframe>
