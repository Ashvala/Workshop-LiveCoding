<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <h2>Pattern Constructors</h2>
    <small>(or: maxi-notation)</small>

    <section>
        <Strudel code={`
s("bd hh sd hh")
// s(seq("bd", "hh", "sd", "hh"))

// s("<bd sd>")
// s(cat("bd", "sd"))

// n("c4,e4,g4")
// n(stack(c4, e4, g4))
// (note variables)

// s("bd|sd")
// s(chooseCycles("bd", "sd"))

// s("~")
// s(silence)

// "0 1 2 3 4 5 6 7".scale('D4 dorian').note()
// run(8).scale('D4 dorian').note()
        `} />
    </section>

    <section>
        <Strudel code={`
stack(
  s(stack(
    "[bd:0|bd:1] <sd:1 sd:2>",
    "[hh oh] <hh hh*2 hh*3 hh*4>",
  )),
  stack(
    "<a4 g4 e4 [d4 <c4 [e4 g4]>]>",
    "a3*<1@3 2>!2 <g3 e3 f#3 g3>!2",
  ).note(),
)
        `} />
    </section>

    <section>
        <iframe width=1000 height=500 src="https://strudel.tidalcycles.org/learn/factories" title="Strudel Docs" />
    </section>
</Slide>
