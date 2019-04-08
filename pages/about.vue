<template>
  <section class="container">
    <div class="poster">
      <img class="my-photo" src="~assets/images/totoro.jpg" />
      <div class="profile">
        <h1>天沼 海彦</h1>
      </div>
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

.poster {
  background-color: #eee;
  width: 750px;
  padding: 20px;
  position: relative;
  z-index: 1;
  display: flex;
  border-radius: 6px;
}

.my-photo {
  width: 45%;
  object-fit: contain;
}

.profile {
  margin-left: 40px;
  padding: 50px 0;
}
</style>

