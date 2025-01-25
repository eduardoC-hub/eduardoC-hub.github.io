
  <script>
    import { onMount } from "svelte";
  
    let cars = [
      { name: "Ferrari 488", price: "$280,000", image: "https://via.placeholder.com/300", description: "A high-performance sports car with a V8 engine and stunning design." },
      { name: "Lamborghini Aventador", price: "$393,000", image: "https://via.placeholder.com/300", description: "A supercar with a powerful V12 engine and unmatched luxury." },
      { name: "Rolls-Royce Phantom", price: "$460,000", image: "https://via.placeholder.com/300", description: "The epitome of elegance and sophistication in luxury vehicles." },
    ];
  
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
        alert(`${car.name} has been added to your favorites!`);
      } else {
        alert(`${car.name} is already in your favorites.`);
      }
    }
  
    function removeFromFavorites(car) {
      favoriteCars = favoriteCars.filter(favCar => favCar !== car);
      alert(`${car.name} has been removed from your favorites.`);
    }
  </script>
  
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css"
    rel="stylesheet"
    integrity="sha384-oTB1D2DRj/qB3UUAsb0x2Djq2v6wtAq3orFl4Bp1DxtDqktwkpPpLLUMflRRXHvH"
    crossorigin="anonymous"
  />
  <div class="container">
    <h1>Bem-vindo à outra página!</h1>
    <a class = "btn" href = "/DW1">Voltar</a>
  </div>
  <div class="container py-5">
    <h1 class="text-center mb-4">Luxury Cars</h1>
    <div class="row g-4">
      {#each cars as car}
        <div class="col-md-4">
          <div class="card h-100">
            <img src={car.image} class="card-img-top" alt={car.name} />
            <div class="card-body">
              <h5 class="card-title">{car.name}</h5>
              <p class="card-text">{car.description}</p>
              <p class="card-text">Price: {car.price}</p>
              <button class="btn btn-primary" on:click={() => showDetails(car)}>
                View Details
              </button>
              <button class="btn btn-warning mt-2" on:click={() => addToFavorites(car)}>
                Add to Favorites
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
      <h2>Your Favorite Cars</h2>
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
        <p>No favorite cars yet. Add some!</p>
      {/if}
    </div>
  </div>
  
  <style>
    .container {
      text-align: center;
      padding: 20px;
    }
    .card {
      transition: transform 0.3s, box-shadow 0.3s;
    }
  
    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
    }
  
    .favorite-list {
      margin-top: 2rem;
    }
  </style>