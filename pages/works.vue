<template>
  <section class="container">
    <div class="card-box">
      <div class="card" v-for="work in works" :key="work.id">
        <img class="card-image" :src="work.image" />
        <div class="card-text">
          <h2>{{work.name}}</h2>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({}) {
    let result = await axios.get('https://umi-portfolio-api.herokuapp.com/api/works/?format=json');
    const works = result.data;
    return { works };
  },
}
</script>

<style>
.container {
  min-height: calc(100vh - 60px);
  width: 100vw;
  background-image: url('~assets/images/oya_nyanko.jpg');
  background-size: cover;
  background-position: center center;
}

.card-box {
  max-width: 100%;
  height: 100%;
  padding: 0;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  position: relative;
  z-index: 1;
}

.card {
  border-radius: 4px;
  margin: 20px;

}

.card-image {
  width: 400px;
  height: 300px;
  object-fit: cover;
  padding: 10px;
  background-color: #eee;
  border-radius: 4px;
}

.card-text {
  margin-top: 4px;
}
h2 {
  display: inline-block;
  background-color: #fff;
  border: 1px solid #000;
  padding: 2px 6px;
  border-radius: 2px;
}
</style>
