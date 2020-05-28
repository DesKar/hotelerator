<script>
  import Hotel from "./components/Hotel.svelte";
  import Search from "./components/SearchBar.svelte";

  let hotels = [];
  let roomTypes = [];

  fetch("data.json")
    .then(response => response.json())
    .then(data => {
      hotels = data[1].entries;
      roomTypes = data[0].roomtypes;
    });
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <div class="container mt-4">
    <Search />
    {#each hotels as hotel}
      <Hotel {...hotel} />
    {/each}
  </div>
</main>
