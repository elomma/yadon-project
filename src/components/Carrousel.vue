<template>
  <div class="carrousel-wrap">
    <img src="@/assets/carrousel.png" class="carrousel-img">
    <img src="@/assets/carrouselMobile.png" class="carrousel-img-mobile">
  </div>
</template>


<style lang="scss">

.carrousel-wrap{
  width: 100vw;
}

.carrousel-img{
  width: 100vw;
}

.carrousel-img-mobile{
  width: 100vw;
  display: none;
}

@media screen and (max-width: 1100px) {

  .carrousel-img{
    display: none;
  }

  .carrousel-img-mobile{
    display: block;
  }
}

</style>

<script>
</script>

