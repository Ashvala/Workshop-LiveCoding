<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <section>
        <h1>THANK YOU</h1>

        <h2>Questions? Comments?<br/>Let us know.</h2>
    </section>

    <section>
        <h1>⚡🌀 FREE TIME 🌀⚡</h1>
    </section>

    <section>
        <Strudel code={`
stack(
  note("[f#2,a#3](3,8)*2 [a3,c#3](3,8)*2").slow(4).s("piano").gain("0.9 1 1.1 1.2").decay("0.1 0.2 0.3 0.4 0.5").release(0.1).sustain(0.1).delay(0.5).lpf(sine.slow(32).mul(5000).add(200)),
  "0 2 4 7 2 4 5 6".degrade().scale(seq('F#2 mixolydian', 'A2 major').slow(4)).note().s("square").legato(0.5).decay(0.3).sustain(0).bpf(sine.slow(4).mul(2000).add(200)).bpq(0.5),
  s("hh*8(<3 5 6 8>,8)").gain(rand.mul(0.6)).delay(0.2),
  s("bd:4 <sd:1!3 sd:1*2>").lpf(perlin.mul(5000)),
).pianoroll({ fold: 1 })
`} />
    </section>

    <section>
        <Strudel code={`
"<C^7 Eb^7 <Dm7 F^7> C#^7>".layer(
  x => x.voicings('lefthand').struct("x [~ x] [~ x?] [x ~]").note().bandf(perlin.mul(500).add(300)),
  x => x.rootNotes(5).add("<0 7>/8").note().s('sawtooth').cutoff(800).legato(0.7).room(0.3),
)
        `} />
    </section>

    <section>
        <Strudel code={`
stack(
  s("bd cp?").hpf(saw.mul(2000).slow(8)),
  note("<c3 c3 [~ [eb3|g3]] [~ [d3|f3]]>").jux(rev).s("square").gain(0.5).lpf(1000).decay(0.25).sustain(0)
)
        `} />
    </section>

    <section>
        <Strudel code={`
stack(
  stack(
    "<c e f g>/<1!4 2!4>",
    "g4 e4 d4 c4 g4 a4 <[c5 ~]!3 [b4 c5]>@2",
  ).note(),
  s("bd hh:1*2").delay(sine.slow(2)).lpf(saw.mul(3000).slow(4)),
)
        `} />
    </section>

    <section>
        <Strudel code={`
await loadOrc('github:kunstmusik/csound-live-code/master/livecode.orc')

stack(
  note("C2@2 C2 [~ Bb1] C2 Bb1 G1@2 Eb2 [F2 G2] D2 [Eb2 F2] C2 Bb1 C2@2").slow(4).csound('Bass').gain(4),
  s("bd*2,[~ hh]*2,~ cp").bank('RolandTR909').lpf(perlin.slow(4).mul(6000))
)
        `} />
    </section>
</Slide>
