<script>
  import { base } from "$app/paths";
</script>

<nav>
  <a href="{base}/">Home</a>
  <a href="{base}/projects">Projects</a>
  <a class="current" href="{base}/contact">Contact</a>
  <a href="{base}/resume">Resume</a>
  <a href="https://github.com/wesleyshe" target="_blank">GitHub</a>
</nav>

<h1>Contact</h1>

<form action="mailto:wesleys@mit.edu" method="GET">
  <label>
    Your email:
    <input name="email" type="email" />
  </label>

  <label>
    Subject:
    <input name="subject" />
  </label>

  <label>
    Message:
    <textarea name="body"></textarea>
  </label>

  <button>Send</button>
</form>
