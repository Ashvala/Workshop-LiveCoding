<script> 
    import { onMount } from 'svelte';
    import Slide from '../lib/Slide.svelte';
</script> 
<Slide> 
    <h3> Strudel 101: What is Strudel? </h3>
    <section data-auto-animate> 
        <div class="r-hstack" style="font-size: 0.9em">
            A type of layered pastry with a filling that is usually sweet, but savoury fillings are also common. It became popular in the 18th century throughout the Habsburg Empire.
            <img src="https://upload.wikimedia.org/wikipedia/commons/4/40/Strudel.jpg" />
        </div>
    </section>    

    <section data-auto-animate> 

        <ul>
            <li> Strudel is a live coding environment derived from Tidal Cycles. </li>
            <li> Pattern-driven - and displays where you are in each pattern! </li>
            <li> Can interface with other browser-compatible audio languages like Csound </li>
            <li> It can even import sounds from Freesound, GitHub, or arbitrary URLs! </li>
        </ul>

    </section>
</Slide>
