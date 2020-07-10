<script>
  import Nav from "../components/Nav.svelte";
  import Content from "../components/Content.svelte";
  export let segment;
</script>

<Nav {segment} />

<main>
  <slot />
</main>

<Content {segment} />
