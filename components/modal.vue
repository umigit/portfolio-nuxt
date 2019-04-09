<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-body">
        <h1 class="modal-title">{{val.name}}</h1>
          <div class="modal-content">
            <img class="modal-image" :src="val.image">
            <div class="modal-text">
              <p>{{val.detail}}</p>
              <div class="modal-link" v-if="val.name !== 'Portfolio'">
                <a :href="val.url">{{val.name}}</a>
                <a :href="val.github_front">GitHub</a>
              </div>
              <div class="modal-link" v-else>
                <a :href="val.url">{{val.name}}</a>
                <a :href="val.github_front">GitHub(Front End)</a>
                <a :href="val.github_back">GitHub(Back End)</a>
              </div>
            </div>
          </div>
          <button @click="$emit('close')">Close</button>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'Modal',
  props: {
    val: Object
  },
}
</script>

<style>
.modal-mask {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;
  background-color: rgba(0,0,0,0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.modal-body {
  background-color: #eee;
  max-width: 900px;
  margin: 20px;
  padding: 20px;
}

.modal-title {
  margin-bottom: 16px;
}

.modal-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.modal-image {
  width: 360px;
  height: 270px;
  object-fit: cover;
}

.modal-text {
  white-space: pre-wrap;
  text-align: left;
  margin-left: 20px;
  padding: 20px 0;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #36967a;
  font-size: 16px;
}

@media screen and (max-width: 479px) {
  .modal-body {
    max-width: 460px;
    font-size: 14px;
  }

  .modal-image {
    width: 280px;
    height: 210px;
  }
}
</style>
