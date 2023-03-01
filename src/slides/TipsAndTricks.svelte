<script>
    import Slide from '../lib/Slide.svelte'
    import Strudel from '../lib/Strudel.svelte'
</script>

<Slide>
    <h2>Miscellaneous Tips & Tricks</h2>

    <section data-markdown data-separator-notes="^Note:">
- Keyboard shortcuts
- Built-in reference
- Single vs. double quotes
- Piano roll
- `.log()`
- Importing sounds
- Importing Csound!
- OSC & MIDI
- Shabda

Note:
Strudel has some basic built-in synthesizers. By default it uses a sawtooth synthesizer. (You can also pull in Csound orchestra files or output MIDI to use custom synths!)
Strudel has 826 built-in sample banks, and you can import custom sounds from anywhere on the web (including Freesound & GitHub).
When attaching sounds to note patterns, they get pitch-shifted. You can set the base pitch to the note you want and the sounds will get pitch shifted appropriately.
    </section>

    <!-- TODO include some examples where relevant -->
</Slide>
