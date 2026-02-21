<script>
    import projects from "$lib/projects.json";
    import reading from "$lib/reading.json";
    import Project from "$lib/Project.svelte";
    import ReadingItem from "$lib/ReadingItem.svelte";
</script>

<nav>
    <a class="current" href="/">Home</a>
    <a href="/projects">Projects</a>
    <a href="/contact">Contact</a>
    <a href="/resume">Resume</a>
    <a href="https://github.com/wesleyshe" target="_blank">GitHub</a>
</nav>

<h1>Ikea Shark</h1>
<p>
    Born in the deep blue aisle and raised on flat pack dreams, this
    distinguished aquatic gentleman has dedicated his life to comfort, loyalty,
    and looking mildly concerned on your behalf. He possesses the quiet
    confidence of someone who knows he is both apex predator and premium pillow,
    a rare dual specialization that few dare attempt.
</p>
<p>
    He thrives in domestic waters such as beds, sofas, and any location that
    recently experienced emotional turbulence. His hobbies include supervising
    naps, participating in dramatic staring contests with the wall, and arriving
    instantly the moment someone says, "I just need a hug." He does not ask
    questions, he simply absorbs vibes and occasionally crumbs.
</p>
<p>
    Despite a fierce reputation, his daily schedule mostly involves heroic
    levels of loafing. He believes in work life balance, especially the life
    part, and has made it his mission to ensure no human within flopping
    distance ever feels unsupported. Scientists remain baffled by how he manages
    to be structured yet squishy, brave yet baby. If found adrift, please return
    to the nearest blanket. Payment can be made in head pats and being included
    in important conversations he will absolutely not repeat.
</p>
<img src="image/ikea%20shark.jpg" alt="my face" />

<h2>Latest Projects</h2>
<div class="projects highlights">
    {#each projects.slice(0, 3) as p}
        <Project data={p} />
    {/each}
</div>

<h2>What I'm Reading</h2>
<div class="reading">
    {#each reading as item}
        <ReadingItem data={item} />
    {/each}
</div>

<style>
    img {
        display: block;
        width: 100%;
        height: auto;
        margin: 0 auto;
    }
    .reading {
        display: flex;
        flex-direction: column;
        gap: 1.25em;
    }
</style>
