<template>
  <section class="container">
    <modal :val="postItem" v-if="showModal" @close="closeModal"></modal>
    <div class="card-box">
      <div class="card" v-for="work in works" :key="work.id">
        <img class="card-image" :src="work.image" @click="openModal(work)"/>
        <div class="card-text">
          <h2>{{work.name}}</h2>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
import modal from '~/components/modal'

export default {
  async asyncData({}) {
    let result = await axios.get('https://umi-portfolio-api.herokuapp.com/api/works/?format=json');
    const works = result.data;
    return { works };
  },
  components: {
    modal,
  },
  data() {
    return {
      showModal: false,
      postItem: '',
    }
  },
  methods: {
    openModal(item) {
      this.postItem = item;
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
  },
}
</script>

<style>
.container {
  min-height: 100vh;
  width: 100vw;
  background-image: url('~assets/oya_nyanko.jpg');
  background-size: cover;
  background-position: center center;
  padding-top:60px;
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
  width: 320px;
  height: 240px;
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
