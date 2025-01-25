<script>
    let menuOpen = false;
    let location = "Rua das Flores, 123 - Centro, São Paulo, SP";
  
    function toggleMenu() {
      menuOpen = !menuOpen;
    }
  </script>
  
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
  
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #ff7eb3, #ff758c);
      color: white;
      line-height: 1.6;
    }
  
    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      background-color: rgba(0, 0, 0, 0.6);
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
    }
  
    header h1 {
      font-size: 2rem;
    }
  
    nav {
      display: flex;
      gap: 1.5rem;
    }
  
    nav a {
      text-decoration: none;
      color: white;
      font-size: 1.2rem;
      transition: color 0.3s;
    }
  
    nav a:hover {
      color: #ffb3c7;
    }
  
    .menu-button {
      background: none;
      border: 2px solid white;
      border-radius: 0.5rem;
      color: white;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }
  
    .menu-button:hover {
      background: white;
      color: #ff7eb3;
    }
  
    .hero {
      text-align: center;
      padding: 4rem 2rem;
      margin: 0 auto;
    }
  
    .hero h2 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
  
    .hero p {
      font-size: 1.2rem;
      max-width: 600px;
      margin: 0 auto;
    }
  
    .button-group {
      margin-top: 2rem;
    }
  
    .button-group a {
      text-decoration: none;
      display: inline-block;
      background-color: #ffb3c7;
      color: white;
      padding: 0.75rem 1.5rem;
      border-radius: 1rem;
      font-size: 1.1rem;
      margin: 0 0.5rem;
      transition: background 0.3s;
    }
  
    .button-group a:hover {
      background-color: #ff758c;
    }
  
    .info-section {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      padding: 2rem;
    }
  
    .info-card {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 1rem;
      padding: 1.5rem;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
      text-align: center;
    }
  
    .info-card h3 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }
  
    .info-card p {
      font-size: 1rem;
      color: #f8f8f8;
    }
  
    .contact-section {
      background-color: rgba(0, 0, 0, 0.6);
      padding: 2rem;
      text-align: center;
    }
  
    .contact-section h3 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }
  
    .location {
      font-size: 1.2rem;
      margin-bottom: 1.5rem;
    }
  
    .contact-button {
      background-color: #ffb3c7;
      color: white;
      padding: 1rem 2rem;
      border-radius: 1rem;
      font-size: 1.2rem;
      text-decoration: none;
      transition: background 0.3s;
    }
  
    .contact-button:hover {
      background-color: #ff758c;
    }
  </style>
  
  <main>
    <header>
      <h1>Loja Feminina</h1>
      <nav>
        <a href="#sobre">Sobre</a>
        <a href="#produtos">Produtos</a>
        <a href="#contato">Contato</a>
        <button class="menu-button" on:click={toggleMenu}>
          {menuOpen ? 'Fechar Menu' : 'Menu'}
        </button>
      </nav>
    </header>
  
    <section class="hero">
      <h2>Bem-vinda à sua nova loja favorita!</h2>
      <p>Descubra roupas incríveis para todas as ocasiões. Compre com estilo, confiança e conforto!</p>
      <div class="button-group">
        <a href="#produtos">Ver Produtos</a>
        <a href="#sobre">Saiba Mais</a>
      </div>
    </section>
  
    <section id="sobre" class="info-section">
      <div class="info-card">
        <h3>Moda Exclusiva</h3>
        <p>Peças únicas e exclusivas que refletem sua personalidade.</p>
      </div>
      <div class="info-card">
        <h3>Conforto Garantido</h3>
        <p>Roupas feitas com materiais de alta qualidade para o seu conforto.</p>
      </div>
      <div class="info-card">
        <h3>Atendimento Premium</h3>
        <p>Uma experiência de compra personalizada e inesquecível.</p>
      </div>
    </section>
  
    <section id="contato" class="contact-section">
      <h3>Visite-nos ou Entre em Contato</h3>
      <p class="location">Localização: {location}</p>
      <a href="mailto:contato@loja.com" class="contact-button">Fale Conosco</a>
    </section>
  </main>
  