<script>
    export let cart = [];
  
    function removeFromCart(index) {
      cart.splice(index, 1);
      alert('Produto removido do carrinho!');
    }
  
    $: total = cart.reduce((sum, item) => sum + parseFloat(item.price.replace('R$', '').replace(',', '.')), 0).toFixed(2);
  </script>
  
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet">
  
  <style>
    body {
      margin: 0;
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to bottom right, #fef3f7, #ffebef);
    }
  </style>
  
  <main class="container py-5">
    <header class="mb-4 text-center">
      <h1 class="mb-3">Carrinho de Compras</h1>
      <p>{cart.length === 0 ? 'Seu carrinho está vazio!' : 'Confira os produtos selecionados.'}</p>
    </header>
  
    {#if cart.length > 0}
      <div class="table-responsive">
        <table class="table table-striped">
          <thead>
            <tr>
              <th>Produto</th>
              <th>Preço</th>
              <th>Ação</th>
            </tr>
          </thead>
          <tbody>
            {#each cart as item, index}
              <tr>
                <td>{item.name}</td>
                <td>{item.price}</td>
                <td>
                  <button class="btn btn-danger btn-sm" on:click={() => removeFromCart(index)}>Remover</button>
                </td>
              </tr>
            {/each}
          </tbody>
          <tfoot>
            <tr>
              <td><strong>Total:</strong></td>
              <td colspan="2">R$ {total}</td>
            </tr>
          </tfoot>
        </table>
      </div>
    {/if}
  
    <div class="mt-4 text-center">
      <a href="/produtos" class="btn btn-secondary">Continuar Comprando</a>
      {#if cart.length > 0}
        <button class="btn btn-success">Finalizar Compra</button>
      {/if}
    </div>
  </main>
  
  
  