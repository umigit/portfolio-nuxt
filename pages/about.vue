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
  max-width: 900px;
  margin: 20px;
  padding: 20px 0;
  position: relative;
  z-index: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  border-radius: 6px;
}

.my-photo {
  max-height: 360px;
  padding: 0 20px;
  object-fit: contain;
}

.profile {
  padding: 20px;
}

p {
  text-align: left;
}

@media screen and (max-width: 479px) {
  .profile {
    font-size: 14px;
  }
}
</style>

