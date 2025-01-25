<script>
    let products = [
      { id: 1, name: "Vestido Floral", price: 199.9, image: "" },
      { id: 2, name: "Vestido Elegante", price: 249.9, image: "" },
      { id: 3, name: "Conjunto Casual", price: 179.9, image: "" },
      { id: 4, name: "Blusa Estilosa", price: 99.9, image: "" },
    ];
  
    let cart = [];
  
    function addToCart(product) {
      cart = [...cart, product];
    }
  
    function removeFromCart(index) {
      cart = cart.filter((_, i) => i !== index);
    }
  
    $: total = cart.reduce((sum, item) => sum + item.price, 0).toFixed(2);
  </script>
  
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #fef3f7, #ffebef);
    }
  
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 20px;
    }
  
    .card {
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
      overflow: hidden;
      transition: transform 0.2s;
    }
  
    .card:hover {
      transform: scale(1.05);
    }
  
    .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
  
    .card-body {
      padding: 15px;
      text-align: center;
    }
  
    .btn {
      display: inline-block;
      padding: 10px 15px;
      margin: 5px;
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  
    .btn-primary {
      background-color: #007bff;
    }
  
    .btn-danger {
      background-color: #dc3545;
    }
  
    .cart {
      margin-top: 20px;
      padding: 20px;
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
  </style>
  
  <div class="container">
    <h1 class="text-center">Loja de Roupas Femininas</h1>
    <p class="text-center">Escolha os produtos que mais combinam com você!</p>
  
    <div class="row">
      {#each products as product}
        <div class="col-md-3">
          <div class="card">
            <img src={product.image} alt={product.name} />
            <div class="card-body">
              <h5>{product.name}</h5>
              <p>R$ {product.price.toFixed(2)}</p>
              <button class="btn btn-primary" on:click={() => addToCart(product)}>Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      {/each}
    </div>
  
    <div class="cart">
      <h2>Carrinho de Compras</h2>
      {#if cart.length > 0}
        <ul>
          {#each cart as item, index}
            <li>
              {item.name} - R$ {item.price.toFixed(2)}
              <button class="btn btn-danger" on:click={() => removeFromCart(index)}>Remover</button>
            </li>
          {/each}
        </ul>
        <p><strong>Total:</strong> R$ {total}</p>
      {:else}
        <p>O carrinho está vazio.</p>
      {/if}
    </div>
  </div>