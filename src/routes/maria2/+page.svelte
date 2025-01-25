<script>
  let promoMessage = '';
  let catalogVisible = false;

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
<header class="bg-gradient p-5 text-center text-white">
  <h1 class="display-4">Pink Glam</h1>
  <p class="lead">Onde o estilo encontra a sofisticação. Descubra seu próximo look agora.</p>
</header>

<!-- Sobre a loja -->
<section class="container my-5">
  <h2 class="text-center text-primary">Sobre a Pink Glam</h2>
  <p class="text-muted text-center">A Pink Glam é mais do que uma loja, é um conceito de moda. Aqui, as mulheres encontram peças para todas as ocasiões, sempre com o toque de elegância e exclusividade que merecem.</p>
  <p class="text-center">Com um portfólio único e atendimento de primeira, nossa missão é fazer você se sentir incrível todos os dias.</p>
</section>

<!-- Localização -->
<section class="container my-5">
  <h2 class="text-center text-primary">Onde nos Encontrar</h2>
  <p class="text-muted text-center">Visite nossa loja física na Rua das Flores, nº 123, no centro da cidade. Estamos prontos para atendê-la com muito carinho e atenção!</p>
</section>

<!-- Botões interativos -->
<section class="container my-5 text-center">
  <button class="btn btn-warning" on:click={toggleCatalog}>Ver Catálogo</button>
  {#if catalogVisible}
    <div class="mt-3">
      <p>Explore as últimas coleções da Pink Glam e encontre as peças que mais combinam com você!</p>
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

  .header {
    background-color: #ff66b2;
  }

  header {
    background: linear-gradient(45deg, #ff66b2, #ff3385);
  }

  h1 {
    font-family: 'Segoe UI', sans-serif;
    font-weight: bold;
  }

  h2 {
    font-family: 'Segoe UI', sans-serif;
    font-weight: 600;
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

  footer p {
    font-size: 14px;
    color: #ccc;
  }

  .content-section {
    padding: 40px 0;
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 30px;
  }

  .content-section h2 {
    color: hsl(330, 86%, 80%);
  }

  .content-section p {
    font-size: 16px;
    color: #555;
    line-height: 1.6;
  }

  .container {
    max-width: 800px;
  }

  .mt-3 {
    margin-top: 1rem;
  }
</style>
