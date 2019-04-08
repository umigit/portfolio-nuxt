<template>
  <section class="container">
    <div class="poster">
      <img class="my-photo" src="~assets/images/totoro.jpg" />
      <div class="profile">
        <Profile/>
        <ProfileEn/>
      </div>
    </div>
  </section>
</template>

<script>
import Profile from "~/components/Profile";
import ProfileEn from "~/components/ProfileEn";
export default {
  components: {
    Profile,
    ProfileEn,
  }
}
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
  width: 850px;
  padding: 20px;
  position: relative;
  z-index: 1;
  display: flex;
  border-radius: 6px;
}

.my-photo {
  width: 40%;
  object-fit: contain;
}

.profile {
  width: 100%;
  margin-left: 40px;
  padding: 20px 0;
}

p {
  text-align: left;
}
</style>

