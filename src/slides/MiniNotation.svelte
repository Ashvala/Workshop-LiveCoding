<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <h2>Mini Notation Basics</h2>

    <section>
        Sequencing (aka <code>fastcat</code>):

        <Strudel code={`
s("bd")

// s("bd sd")

// s("bd sd hh")

// s("bd hh sd oh")
`} />

        <aside class="note">
            Everything happens in one cycle. If you add more elements to the sequence, the subdivisions get smaller.
        </aside>
    </section>

    <section>
        Nested sequencing:

        <Strudel code={`
s("bd [hh oh]")

// s("bd [sd [hh oh]]")

// s("bd [hh hh hh]")

// s("bd hh*3")
`} />
    </section>

    <section>
        Alternation (aka <code>cat</code>, <code>slowcat</code>):

        <Strudel code={`
s("bd")

// s("<bd sd>")

// s("<bd sd hh>")

// s("bd <hh oh>")
`} />
    </section>

    <section>
        Stacking:
        <Strudel code={`
s("bd")

// s("bd,hh")

// s("bd,hh,sd")

// whoops:
// s("bd,hh sd,hh")

// s("[bd,hh] [sd,hh]")
`} />
    </section>

    <section>
        Choice:
        <Strudel code={`
s("bd")

// s("bd|sd|hh")

// s("bd hh [sd|cp] hh")
`} />
    </section>

    <section>
        Types of elements:
        <Strudel code={`
s("bd hh sd hh")

// s("bd:0 bd:1 bd:2 bd:3")
// s("sd:0 sd:1 sd:2 sd:3")

// n("c d e d")

// mind the octave:
// n("a b c e")

// n("a4 b4 c5 d5 b4@2 g4 a4@5").slow(3)

// n("0 1 2 3 4 5").scale('C4 lydian')

// freq("100 200 300 400 500 600 700 800")
`} />
    </section>
</Slide>
