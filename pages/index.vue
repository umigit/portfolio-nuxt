<template>
  <section class="container">
    <div>
      <img class="title" name="slide" src="~assets/umihiko_800.png"/>
    </div>
  </section>
</template>


<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background-image: url("~assets/oya_nyanko.jpg");
  background-size: cover;
  background-position: center center;
  padding-top:60px;
}

.title {
  max-width: 800px;
  width: 100%;
  object-fit: contain;
  position: relative;
  z-index: 1;
}
</style>
