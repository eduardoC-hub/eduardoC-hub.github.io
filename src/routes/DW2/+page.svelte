<script>
  let greetingMessage = '';
  function showGreeting() {
    greetingMessage = 'Obrigado por visitar nossa loja! Estamos ansiosos para atendê-lo.';
  }
</script>

<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-oTB1D2DRj/qB3UUAsb0x2Djq2v6wtAq3orFl4Bp1DxtDqktwkpPpLLUMflRRXHvH"
  crossorigin="anonymous"
/>

<div class="header">
  <h1>Bem-vindo à <b>Loxious</b></h1>
  <p>Onde o luxo encontra a performance.</p>
  <button class="btn btn-info mt-3" on:click={showGreeting}>Clique para uma saudação especial</button>
  {#if greetingMessage}
    <p class="mt-3 text-success">{greetingMessage}</p>
  {/if}
</div>

<div class="container content-section">
  <h2>Sobre a <b>Loxious</b></h2>
  <p>Localizada em Castilho, no centro da cidade, essa loja oferece uma experiência única para quem busca carros de luxo. Aqui, você encontrará os modelos mais exclusivos, com a qualidade e sofisticação que você merece. Se você está em busca de algo realmente especial, a Loxius é o lugar certo!</p>
  <p>Com um ambiente moderno e uma equipe de profissionais altamente qualificados, garantimos um atendimento personalizado para você escolher o carro dos seus sonhos. Cada detalhe é pensado para sua experiência ser inesquecível.</p>
</div>

<div class="container content-section">
  <h2>Visite-nos</h2>
  <p>Estamos localizados na rua jardim alvorada, nº 784, no coração de castilho. Nossa loja é de fácil acesso e está pronta para receber você.</p>
  <p>Se você procura exclusividade, conforto e um atendimento impecável, venha nos visitar e vivencie a experiência de estar em um verdadeiro showroom de carros de luxo. Nosso time estará à disposição para oferecer uma experiência única!</p>
</div>

<br>
<div class ="center">
<h3>clique no botao a baixo e veja alguns dos nossos melhores carros</h3>

<div class="container text-center">
  <button class="btn btn-primary mt-3" on:click={() => window.location.href = 'https://eduardoc-hub.github.io/DW2'}>Voltar ao inicio</button>
</div>
</div>
<div class="footer">
  <p>&copy; 2025 Loxiuos. Todos os direitos reservados.</p>
  <br>
  <p>siga no instagram @edu_cale S2</p>
</div>

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
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 30px;
  }
  .center {
    text-align: center;
  }
  .content-section h2 {
    color: #343a40;
    text-align: center;
  }

  .content-section p {
    font-size: 16px;
    color: #555;
    line-height: 1.6;
  }

  .btn-info {
    background-color: #17a2b8;
    border: none;
    padding: 10px 20px;
    font-size: 16px;
    transition: background-color 0.3s;
  }

  .btn-info:hover {
    background-color: #138496;
  }

  .btn-primary {
    text-align: center;
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

  .footer p {
    font-size: 14px;
    color: #ccc;
  }
</style>
