<script>
  import { base } from "$app/paths";
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";
</script>

<nav>
  <a href="{base}/">Home</a>
  <a class="current" href="{base}/projects">Projects</a>
  <a href="{base}/contact">Contact</a>
  <a href="{base}/resume">Resume</a>
  <a href="https://github.com/wesleyshe" target="_blank">GitHub</a>
</nav>

<section class="projects">
  <h1>{projects.length} Projects</h1>

  {#each projects as p}
    <Project data={p} />
  {/each}
</section>
