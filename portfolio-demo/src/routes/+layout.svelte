<script lang="ts">
    // Este layout se aplicará a todas las páginas
  // import '../styles/global.css';

  let isDarkMode = true;

  function toggleTheme() {
    isDarkMode = !isDarkMode;
  }

</script>
  
<div class="app" class:dark={isDarkMode}>
  <header>
    <nav>
      <a href="/">Inicio</a>
      <a href="/about">Sobre Mí</a>
      <a href="/projects">Proyectos</a>
      <a href="/contact">Contacto</a>
      <button on:click={toggleTheme}>
        {isDarkMode ? 'Modo Claro' : 'Modo Oscuro'}
      </button>
    </nav>        
  </header>

  <main>
    <!-- Aquí se renderizará el contenido de cada página -->
    <slot />
  </main>

  <footer>
    <slot name="footer">
      <p>© 2025 Sebastián González - Todos los derechos reservados</p>
    </slot>
  </footer>

</div>

<style>

  .app {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

 

  main {
    flex: 1;
    padding: 2rem;
  }

  nav {
    padding: 1rem;
    background: #f4f4f4;

    a {
      margin-right: 1rem;
      color: blue;
      text-decoration: none;
    }

    a:hover {
      color: red;
    }
  }

  /* main {
    padding: 2rem;
    max-width: 1200px;
    margin: 0 auto;
  } */

  footer {
    padding: 1rem;
    text-align: center;
    background: #f4f4f4;
    color: #000000;
  }

  .dark {
    background: #1a1a1a;
    color: #ffffff;

    nav {
      background: #333333;

      a {
        color: #ffffff;
      }

      a:hover {
        color: lightblue;
      }
    }

    footer {
      background: #1a1a1a;
      color: #ffffff;
    }
  }


</style>