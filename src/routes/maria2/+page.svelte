<script>
    let products = [
      { id: 1, name: "Vestido Floral", price: "R$ 199,90", image: "floral.jpg" },
      { id: 2, name: "Vestido Elegante", price: "R$ 249,90", image: "elegante.jpg" },
      { id: 3, name: "Conjunto Casual", price: "R$ 179,90", image: "casual.jpg" },
      { id: 4, name: "Blusa Estilosa", price: "R$ 99,90", image: "estilosa.jpg" },
    ];
  
    let cart = [];
  
    function addToCart(product) {
      cart = [...cart, product];
      alert(`${product.name} foi adicionado ao carrinho!`);
    }
  </script>
  
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css"
    rel="stylesheet"
  />
  
  <style>
    body {
      margin: 0;
      font-family: "Arial", sans-serif;
      background: linear-gradient(to bottom right, #fef3f7, #ffebef);
    }
  
    .card {
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
  
    .card img {
      border-top-left-radius: 0.5rem;
      border-top-right-radius: 0.5rem;
    }
  
    .btn-custom {
      background-color: #ff7eb3;
      color: white;
      border: none;
    }
  
    .btn-custom:hover {
      background-color: #ff4d85;
    }
  </style>
  
  <main class="container py-5">
    <header class="mb-4 text-center">
      <h1 class="mb-3">Produtos Disponíveis</h1>
      <p>Escolha as melhores roupas para o seu estilo!</p>
    </header>
  
    <div class="row g-4">
      {#each products as product}
        <div class="col-md-3">
          <div class="card">
            <img src={product.image} class="card-img-top" alt={product.name} />
            <div class="card-body">
              <h5 class="card-title">{product.name}</h5>
              <p class="card-text">{product.price}</p>
              <button class="btn btn-custom" on:click={() => addToCart(product)}>
                Adicionar ao Carrinho
              </button>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </main>
  