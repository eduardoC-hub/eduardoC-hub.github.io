
<script>
import {cars} from '$lib/componentes/carros.js'
  

  let selectedCar = null;
  let favoriteCars = [];

  function showDetails(car) {
    selectedCar = car;
  }

  function clearDetails() {
    selectedCar = null;
  }

  function addToFavorites(car) {
    if (!favoriteCars.includes(car)) {
      favoriteCars = [...favoriteCars, car];
      alert(`${car.name} foi adicionado aos seus favoritos!`);
    } else {
      alert(`${car.name} já está nos seus favoritos.`);
    }
  }

  function removeFromFavorites(car) {
    favoriteCars = favoriteCars.filter(favCar => favCar !== car);
    alert(`${car.name}  foi removido dos seus favoritos.`);
  }
</script>

<link
  href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
  rel="stylesheet"
  integrity="sha384-oTB1D2DRj/qB3UUAsb0x2Djq2v6wtAq3orFl4Bp1DxtDqktwkpPpLLUMflRRXHvH"
  crossorigin="anonymous"
/> 
<div class="borao">
  <button class="borao" on:click={() => window.location.href = 'https://eduardoc-hub.github.io/DW1'}>voltar</button>
</div>
<div class="container py-5">
  <h1 class="text-center mb-4">Esses são três dos nosso carros Luxuoso mais vendidos!</h1>
  <div class="row row-cols-1 row-cols-md-3 g-4">
    {#each cars as car}
      <div class="col">
        <div class="card h-100">
          <img src={car.image} class="card-img-top" alt={car.name} />
          <div class="card-body">
            <h5 class="card-title">{car.name}</h5>
            <p class="card-text">{car.description}</p>
            <p class="card-text">Preço em dolares: {car.price}</p>
            <button class="btn btn-primary" on:click={() => showDetails(car)}>
              ver melhor
            </button>
            <button class="btn btn-warning mt-2" on:click={() => addToFavorites(car)}>
              adicionar aos favoritos
            </button>
          </div>
        </div>
      </div>
    {/each}
  </div>

  {#if selectedCar}
    <div class="modal fade show d-block" tabindex="-1" style="background-color: rgba(0, 0, 0, 0.5);">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">{selectedCar.name}</h5>
            <button type="button" class="btn-close" aria-label="Close" on:click={clearDetails}></button>
          </div>
          <div class="modal-body">
            <img src={selectedCar.image} class="img-fluid mb-3" alt={selectedCar.name} />
            <p>{selectedCar.description}</p>
            <p>Price: {selectedCar.price}</p>
          </div>
          <div class="modal-footer">
            <button class="btn btn-secondary" on:click={clearDetails}>Close</button>
          </div>
        </div>
      </div>
    </div>
  {/if}

  <div class="favorite-list">
    <h2>Seus carros favoritos</h2>
    {#if favoriteCars.length > 0}
      <ul class="list-group">
        {#each favoriteCars as favCar}
          <li class="list-group-item d-flex justify-content-between align-items-center">
            {favCar.name}
            <button class="btn btn-danger btn-sm" on:click={() => removeFromFavorites(favCar)}>
              Remove
            </button>
          </li>
        {/each}
      </ul>
    {:else}
      <p>Sem carros favoritos, adicione algum!</p>
    {/if}
  </div>
</div>

<style>
  .containerone {
    width:100%;
    background-color: aquamarine;
    text-align: center;
    height: 100px;
    display: inline-block;
  }
  .container {
    text-align: center;
    padding: 20px;
    
  }
  
  .card {
    transition: transform 0.3s, box-shadow 0.3s;
    border: none;
    border-radius: 15px;
    overflow: hidden;
  }

  .card:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  }

  .favorite-list {
    display: grid;
    margin-top: 2rem;
    background-color: aqua;
    width: 100%;
    height: 200px;

  }

  .btn-primary {
    background-color: #007bff;
    border: none;
    transition: background-color 0.3s;
  }

  .btn-primary:hover {
    background-color: #0056b3;
  }

  .btn-warning {
    background-color: #f0ad4e;
    border: none;
    transition: background-color 0.3s;
  }

  .btn-warning:hover {
    background-color: #ec971f;
  }

  .modal {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .modal-content {
    border-radius: 15px;
  }
  .card-img-top {
    width: 350px;
    height: 250px; 
    object-fit: cover; 
  }
  .borao{
    position: absolute;
    top: 0;
  }
</style>
