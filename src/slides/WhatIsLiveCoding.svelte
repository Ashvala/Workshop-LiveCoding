<script> 
import Slide from '../lib/Slide.svelte';
</script>

<Slide> 
    <section data-auto-animate data-auto-animate-unmatched="fade">
        <h1>What is live coding?</h1> 
        <h3>Live coding is coding… live. 🤯</h3>
    </section>
    <section data-auto-animate>
        <h1>What is live coding?</h1> 
        <p>Live coding is code-as-performance; the artistic practice of creating music (or visuals, choreography, etc.) in real-time by writing code, which is exposed to the audience rather than hidden away.</p>
    </section>
    <section data-auto-animate>
        <h1>What is live coding?</h1> 
        <p>Per TOPLAP:<p/>
        <blockquote class="quote">
            Live coding is a new direction in electronic music and video, and is getting somewhere interesting. Live coders expose and rewire the innards of software while it generates improvised music and/or visuals. All code manipulation is projected for your pleasure. Live coding works across musical genres, and has been seen in concert halls, late night jazz bars, as well as algoraves. There is also a strong movement of video-based live coders, writing code to make visuals, and many environments can do both sound and video, creating synaesthetic experiences.
        </blockquote>
    </section>
    <section>
        <iframe title="TOPLAP Manifesto" src="https://toplap.org/wiki/ManifestoDraft"></iframe>
    </section>
</Slide>

<style>
    .quote {
        font-size: 0.65em;
        width: 90%;
        margin: 5%;
        text-align: left;
        padding: 0.5em;
    }

    iframe {
        width: 1000px;
        height: 600px;
    }
</style>
