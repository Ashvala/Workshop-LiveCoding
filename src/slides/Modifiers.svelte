<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <h2>Modifiers</h2>

    <section>
        <Strudel code={`
s("hh*4")

// s("hh*4").gain(0.5)

// s("hh*4").lpf(2000)

// s("hh*4").hpf(5000)

// s("hh*2").room(0.2)

// s("hh*4").delaytime(1/8).delay(0.6)

// s("hh*4").crush(4)

// n("c a f e").s('sawtooth')
        `} />
    </section>

    <section>
        <Strudel code={`
s("hh*4")

// s("hh*4").gain(".3 .4 .7 .9")

// s("sd*4").lpf("<100 500 2000 5000>")

// s("hh*2").room("[0|.7]")

// s("hh*4").crush("<16 8 4 2 1>")

// n("c a f e").s("sawtooth square triangle sine")
        `} />

        <aside class="notes">
            Controls can also be patterns!!
        </aside>
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/learn/time-modifiers" title="Strudel Docs" />

        <aside class="notes">
            Too many modifiers to cover; we'll look at the strudel docs to give a sense of the kinds of modifiers that are available.
        </aside>
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/functions/value-modifiers" title="Strudel Docs" />
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/learn/signals" title="Strudel Docs" />
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/learn/conditional-modifiers" title="Strudel Docs" />
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/learn/accumulation" title="Strudel Docs" />
    </section>

    <section>
        <iframe width=1000 height=600 src="https://strudel.tidalcycles.org/learn/tonal" title="Strudel Docs" />
    </section>
</Slide>
