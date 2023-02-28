<script> 
    import { onMount } from 'svelte';
    import Slide from '../lib/Slide.svelte';
</script> 
<Slide> 
    <h2>What is Strudel?</h2>
    <section> 
        <div class="r-hstack" style="font-size: 0.85em">
            <div style="text-align: left; margin-right: 1em">
                A type of layered pastry with a filling that is usually sweet, but savoury fillings are also common. It became popular in the 18th century throughout the Habsburg Empire.<br/>
                <small><em>- Wikipedia, “Strudel”, accessed 2023-02-25</em></small>
            </div>
            <img src="https://upload.wikimedia.org/wikipedia/commons/4/40/Strudel.jpg" alt="Delicious strudel" />
        </div>
    </section>    

    <section>
        <ul>
            <li>Strudel is a live coding environment derived from Tidal Cycles.</li>
            <li>Pattern-driven - and displays where you are in each pattern!</li>
            <li>Can interface with other browser-compatible audio languages like Csound</li>
            <li>It can even import sounds from Freesound, GitHub, or arbitrary URLs!</li>
        </ul>
    </section>

    <section>
        Mostly important for our workshop today:<br/>
        <em>It runs in the browser!</em><br/><br/>
        So you don't need to install or set up anything.<br/>
        Just go to <a href="https://strudal.tidalcycles.org">strudal.tidalcycles.org</a>.
    </section>
</Slide>
