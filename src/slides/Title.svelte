<script>
    import { onMount } from 'svelte'
    import Slide from '../lib/Slide.svelte'

    // Title animation
    // (Yes, I spent too much time on this.)
    let root

    function getTextNodes(node) {
        if (node.nodeName === "#text") {
            return [node]
        }
        return [].concat(...[...node.childNodes].map(getTextNodes))
    }

    function sleep(ms) {
        return new Promise(resolve => setTimeout(resolve, ms))
    }

    function choose(array) {
        return array[Math.floor(Math.random() * array.length)]
    }

    function makeGarbage(s, prob) {
        const symbols = "[]()<>[]{}!@/*%"
        const out = []
        for (const c of [...s]) {
            if (/\S/.test(c) && Math.random() < prob) {
                out.push(choose(symbols))
            } else {
                out.push(c)
            }
        }
        return out.join("")
    }

    onMount(() => {
        const textNodes = getTextNodes(root)
        const originalText = textNodes.map(node => node.nodeValue)
        const animation = async () => {
            const n = 150
            for (let i = 0; i < n; i++) {
                const prob = 1 - (i / n)
                for (const [i, node] of textNodes.entries()) {
                    node.nodeValue = makeGarbage(originalText[i], prob)
                }
                await sleep(60 + 80 * (i + 1) / n)
            }
            for (const [i, node] of textNodes.entries()) {
                node.nodeValue = originalText[i]
            }
        }
        animation()
    })
</script>

<Slide>
    <div bind:this={root} class="code">
        <h1 class="hack">
            LIVE CODING:
        </h1>
        <h2 class="hack">An Introduction</h2>
        <h2> 
            Ash <span class="gray">x</span> IJC
        </h2>
        <small class="gray">(aka M3RGE C0NFL1CT)</small>
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
