<script>
  import { metatags, page } from "@roxi/routify";
  import Navigation from "./_navigation.svelte";
  import Footer from "../components/Footer.svelte";
  $: metatags.title = `My Routify app - ${$page.title}`;
  metatags.description = "Description coming soon...";
</script>

<Navigation />
<slot />
<Footer />