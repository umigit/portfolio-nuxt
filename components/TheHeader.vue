<template>
  <header class="header">
    <div class="header-inner">
      <ul class="navi">
        <li class="navi-item">
          <nuxt-link to="/">HOME</nuxt-link>
        </li>
        <li class="navi-item">
          <nuxt-link to="/about">ABOUT</nuxt-link>
        </li>
        <li class="navi-item">
          <nuxt-link to="/works">WORKS</nuxt-link>
        </li>
        <li class="navi-item">
          <nuxt-link to="/skills">SKILLS</nuxt-link>
        </li>
        <li class="navi-item">
          <nuxt-link to="/links">LINKS</nuxt-link>
        </li>
      </ul>
    </div>
  </header>
</template>

<style>
.header {
  height: 60px;
  width: 100vw;
  background-color: #eee;
  position: fixed;
  z-index: 1;
}

.header-inner {
  height: 100%;
  padding: 0;
  text-align: center;
  position: relative;
}

.navi {
  max-width: 100vw;
  display: inline-flex;
  list-style: none;
  margin: 0;
  padding: 0;
  position: absolute;
  left: 50%;
  bottom: 0;
  transform: translate(-50%, 0);
}

.navi-item > a {
  color: #000;
  display: block;

  text-decoration: none;
}

a:visited {
  color: #000;
}

a:hover {
  color: #fff;
  background-color: rgba(54,150,122,0.5);
}

.nuxt-link-exact-active {
  color: #fff;
  background-color: rgb(54,150,122);
}

.nuxt-link-exact-active:visited {
  color: #fff;
}

@media screen and (min-width: 480px) {
  .navi-item > a {
    padding: 10px 20px;
  }
}

@media screen and (max-width: 479px) {
 .navi-item > a {
    padding: 10px 5px;
    font-size: 14spx;
  }
}
</style>
