<script lang="ts">
  import Card from '$lib/components/Card.svelte';

  // Estado local
  let count = 0;

  // Método
  function incrementCount() {
    count += 1;
  }
</script>
  
<h1>Bienvenido a mi portafolio</h1>
  
<Card 
  title="Sobre este sitio" 
  description="Este es un portafolio construido con SvelteKit"
>
  <button on:click={incrementCount}>
    Clicks: {count}
  </button>
</Card>
  
<style>
  h1 {
    color: #333;
    font-size: 2rem;
  }

  button {
    padding: 0.5rem 1rem;
    background: #0066cc;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
</style>