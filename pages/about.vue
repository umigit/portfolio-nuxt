<template>
  <section class="container">
    <div class="poster">
      <img class="my-photo" src="~assets/at_cafe.png" />
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

.poster {
  background-color: #eee;
  width: 80%;
  max-width: 950px;
  margin: 20px;
  padding: 20px 0;
  position: relative;
  z-index: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
}

.my-photo {
  max-height: 360px;
  width: 40%;
  padding: 20px;
  object-fit: contain;
}

.profile {
  padding: 20px;
  flex: 1;
}

p {
  text-align: left;
}

@media screen and (max-width: 959px) {
  .poster {
    width: 100%;
  }
}

@media screen and (max-width: 519px) {
  .poster {
    flex-direction: column;
    align-items: center;
  }

  .my-photo {
    width: 60%;
  }

  .profile {
    font-size: 14px;
  }
}

</style>

