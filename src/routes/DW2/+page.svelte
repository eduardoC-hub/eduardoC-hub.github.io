<script>
  // Aqui podemos ter algum código de navegação ou outras funcionalidades
</script>

<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-oTB1D2DRj/qB3UUAsb0x2Djq2v6wtAq3orFl4Bp1DxtDqktwkpPpLLUMflRRXHvH"
  crossorigin="anonymous"
/>

<style>
  body {
    background-color: #f8f9fa;
    font-family: 'Arial', sans-serif;
  }

  .header {
    background-color: #343a40;
    color: white;
    padding: 40px 0;
    text-align: center;
  }

  .content-section {
    padding: 40px 0;
    text-align: center;
  }

  .content-section h2 {
    color: #343a40;
  }

  .btn-primary {
    background-color: #007bff;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    transition: background-color 0.3s;
  }

  .btn-primary:hover {
    background-color: #0056b3;
  }

  .footer {
    background-color: #343a40;
    color: white;
    text-align: center;
    padding: 20px;
  }
</style>

<div class="header">
  <h1>Bem-vindo à loxius</h1>
  <p>Onde o luxo encontra a performance.</p>
</div>

<div class="container content-section">
  <h2>Sobre a Nossa Loja</h2>
  <p>Localizada no coração da cidade, a nossa loja oferece uma experiência única para quem busca carros de luxo. Aqui, você encontrará os modelos mais exclusivos, com a qualidade e sofisticação que você merece.</p>
  <p>Com um ambiente moderno e uma equipe de profissionais altamente qualificados, garantimos um atendimento personalizado para você escolher o carro dos seus sonhos.</p>
</div>

<div class="container content-section">
  <h2>Visite-nos</h2>
  <p>Estamos localizados na Avenida das Américas, nº 2000, no centro da cidade. Nossa loja é de fácil acesso e está pronta para receber você.</p>
  <p>Se você procura exclusividade, conforto e um atendimento impecável, venha nos visitar e vivencie a experiência de estar em um verdadeiro showroom de carros de luxo.</p>
</div>

<div class="container text-center">
  <button class="btn btn-primary" on:click={() => window.location.href = 'https://eduardoc-hub.github.io/DW3'}>Ver Carros</button>
</div>

<div class="footer">
  <p>&copy; 2025 Loja de Carros Luxuosos. Todos os direitos reservados.</p>
</div>
