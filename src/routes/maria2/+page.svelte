<script>
  let greetingMessage = '';
  let promoMessage = '';
  let catalogVisible = false;

  function showGreeting() {
    greetingMessage = 'Bem-vinda à Pink Glam! Adoramos ajudar você a encontrar o look perfeito.';
  }

  function showPromo() {
    promoMessage = 'Use o código VERÃO20 para ganhar 20% de desconto em todas as peças de verão!';
  }

  function toggleCatalog() {
    catalogVisible = !catalogVisible;
  }
</script>

<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-oTB1D2DRj/qB3UUAsb0x2Djq2v6wtAq3orFl4Bp1DxtDqktwkpPpLLUMflRRXHvH"
  crossorigin="anonymous"
/>

<!-- Cabeçalho -->
<header class="bg-primary text-white text-center p-4">
  <h1 class="display-4">Pink Glam</h1>
  <p>Onde o estilo e a sofisticação se encontram</p>
</header>

<!-- Saudação -->
<section class="container my-5 text-center">
  <button class="btn btn-outline-light" on:click={showGreeting}>Clique para uma saudação</button>
  {#if greetingMessage}
    <p class="mt-3 text-success">{greetingMessage}</p>
  {/if}
</section>

<!-- Sobre a loja -->
<section class="container my-5">
  <h2 class="text-center text-primary">Sobre a Pink Glam</h2>
  <p class="text-muted text-center">Localizada no coração da cidade, a Pink Glam oferece roupas que combinam estilo e sofisticação.</p>
  <p class="text-center">Nossa missão é proporcionar a você as últimas tendências da moda para que você se sinta única e especial.</p>
</section>

<!-- Localização -->
<section class="container my-5">
  <h2 class="text-center text-primary">Visite-nos</h2>
  <p class="text-muted text-center">Estamos na Rua das Flores, nº 123, no centro da cidade. Venha nos visitar e se apaixonar pelas nossas coleções.</p>
</section>

<!-- Botões interativos -->
<section class="container my-5 text-center">
  <button class="btn btn-warning" on:click={toggleCatalog}>Ver Catálogo</button>
  {#if catalogVisible}
    <div class="mt-3">
      <p>Descubra as últimas coleções da Pink Glam e escolha suas peças favoritas!</p>
    </div>
  {/if}

  <button class="btn btn-success mt-3" on:click={showPromo}>Ver Promoção</button>
  {#if promoMessage}
    <p class="mt-3 text-danger">{promoMessage}</p>
  {/if}
</section>

<!-- Rodapé -->
<footer class="bg-dark text-white text-center p-4">
  <p>&copy; 2025 Pink Glam. Todos os direitos reservados.</p>
  <p>Siga-nos no Instagram @pinkglam_oficial</p>
</footer>

<style>
  body {
    font-family: 'Arial', sans-serif;
    background-color: #f8f9fa;
  }

  h1, h2 {
    font-family: 'Segoe UI', sans-serif;
  }

  .btn-outline-light {
    border-color: #fff;
    color: #fff;
  }

  .btn-outline-light:hover {
    background-color: #ff66b2;
  }

  .btn-warning {
    background-color: #ffcc00;
    color: white;
  }

  .btn-warning:hover {
    background-color: #e6b800;
  }

  .btn-success {
    background-color: #28a745;
    color: white;
  }

  .btn-success:hover {
    background-color: #218838;
  }

  footer {
    background-color: #333;
    color: white;
  }
</style>
