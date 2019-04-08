<template>
  <section class="container">
    <div>
      <img class="title" name="slide" src="~assets/images/umihiko_800.png"/>
    </div>
  </section>
</template>

<script>
</script>

<style>
.container {
  min-height: calc(100vh - 60px);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-image: url("~assets/images/oya_nyanko.jpg");
  background-size: cover;
  background-position: center center;
}

.title {
  max-width: 800px;
  width: 100%;
  object-fit: contain;
  position: relative;
  z-index: 1;
}
</style>
