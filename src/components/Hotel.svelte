<script>
  import HotelInfo from "./HotelInfo.svelte";
  export let hotelName;
  export let rating;
  export let city;
  export let thumbnail;
  export let guestrating;
  export let ratings;
  export let mapurl;
  export let filters;
  export let price;
</script>

<style>
  img {
    width: 100%;
  }
  .price {
    vertical-align: middle;
    color: green;
    font-size: 180%;
  }
</style>

<div class="container-fluid shadow p-2 mb-2 bg-white rounded">
  <div class="row">
    <div class="col-sm">
      <img src={thumbnail} alt={hotelName} />
    </div>
    <div class="col-sm">
      <HotelInfo {hotelName} {rating} {city} {ratings} {guestrating} />
    </div>
    <div class="col-sm price">
      &euro {price}<br>
      <button class="btn btn-success m-4"><strong>View Deal</strong></button>
    </div>

  </div>
</div>
