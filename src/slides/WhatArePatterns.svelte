<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <h2>What are patterns?</h2>

    <section>
        <Strudel code={`
// licensed with CC BY-NC-SA 4.0 https://creativecommons.org/licenses/by-nc-sa/4.0/
// by Felix Roos
stack(
    s("bd*2,~ [cp,sd]").bank('RolandTR909'),
    
    s("hh:1*4").sometimes(fast("2"))
    .rarely(x=>x.speed(".5").delay(.5))
    .end(perlin.range(0.02,.05).slow(8))
    .bank('RolandTR909').room(.5)
    .gain("0.4,0.4(5,8,-1)"),
    
    note("<0 2 5 3>".scale('G1 minor')).struct("x(5,8,-1)")
    .s('sawtooth').decay(.1).sustain(0),
    
    note("<G4 A4 Bb4 A4>,Bb3,D3").struct("~ x*2").s('square').clip(1)
    .cutoff(sine.range(500,4000).slow(16)).resonance(10)
    .decay(sine.slow(15).range(.05,.2)).sustain(0)
    .room(.5).gain(.3).delay(.2).mask("<0 1@3>/8"),
    
    "0 5 3 2".sometimes(slow(2)).off(1/8,add(5)).scale('G4 minor').note()
    .decay(.05).sustain(0).delay(.2).degradeBy(.5).mask("<0 1>/16")
)`} />
    </section>

    <section>
        <p>Consider typing out a melody. For example:</p>

        <Strudel code='note("c d e g c d e ab c d e a c d e bb").cpm(10)' />

        <p>A bit unwieldy. What is the underlying structure? What if you want to change it?</p>
    </section>

    <section>
        <p>With patterns, this can be compressed:</p>

        <Strudel code='note("c d e <g ab a bb>").cpm(40)' />

        <p>This expresses the fact that the melody consists of a four-note cells, with only the last note changing.</p>

        <aside class="notes">
            <p>
                In this trivial example, we used the angle bracket notation (<em>slowcat</em>) to reduce duplication and make the pattern more clear. Many other operators and pattern functions exist, and we'll cover several of them today.
            </p>
            <p>
                The key point is that patterns allow you to <em>express musical ideas concisely</em>: in particular, as <em>compositions of simpler patterns!</em>
            </p>
            <p>
                A key feature of patterns is that you can modify patterns using other patterns. For example, you can stack patterns together, concatenate patterns, or modulate effects with another pattern.
Strudel includes many functions to combine patterns in different ways, and learning how (and when) to use them is key to mastering the language.
            </p>
        </aside>
    </section>
</Slide>
