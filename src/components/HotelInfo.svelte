<script>
  export let hotelName;
  export let rating;
  export let city;
  export let guestrating;
  export let ratings;

  let stars = "";
  for (let i = 0; i < 5; i++) {
    if (i < rating) {
      stars += "&#9733; ";
    } else {
      stars += "&#9734; ";
    }
  }
</script>

<style>
  .star {
    color: yellow;
  }
</style>

<div class="p-2">
  <strong>{hotelName}</strong>
</div>
<div class="p-2 star">
  {@html stars}
</div>
<div class="p-2">{city}</div>
<div class="mb-2">
  {ratings.no}
  <strong>{ratings.text}</strong>
</div>
<div>Guest rating: {guestrating}</div>
