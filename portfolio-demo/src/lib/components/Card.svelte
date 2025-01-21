<script lang="ts">
  // Props del componente
  export let title: string;
  export let description: string;
</script>
  
<div class="card">
  <h2>{title}</h2>
  <p>{description}</p>
  <slot />
</div>

<style>
  .card {
    padding: 1rem;
    border: 1px solid #ddd;
    border-radius: 8px;
    margin: 1rem 0;
  }
</style>