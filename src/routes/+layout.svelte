<script lang="ts">
  import Header from '$lib/header/Header.svelte';
  import { onMount } from 'svelte';
  import '../app.css';

  onMount(() => {
    console.log(window.innerHeight);
    console.log(window.outerHeight);
    window.addEventListener('scroll', (e) => {
      console.log(e);
    });
  });
</script>

<svelte:head>
  <title>Parti MUDA | N9</title>
  <meta name="description" content="Offical site of Parti MUDA N9 (Negeri Sembilan)" />
</svelte:head>

<main style="height: 1000px;">
  <slot />
</main>

<footer>
  © 2022. Designed by <a href="https://www.linkedin.com/in/sian-loong-7b4a3037/" target="_blank"
    >SianLoong</a
  > for MUDA
</footer>

<style>
  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    width: 100%;
    max-width: 1024px;
    margin: 0 auto;
    box-sizing: border-box;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px;
  }

  footer a {
    font-weight: bold;
  }

  @media (min-width: 480px) {
    footer {
      padding: 40px 0;
    }
  }
</style>
