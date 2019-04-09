<template>
  <div class="container">
    <div class="link-card">
      <ul class="link-list">
        <li class="link-item">
          <h3>Twitter: <a href="//twitter.com/umi_david">@umi_david</a></h3>
        </li>
        <li class="link-item">
          <h3>Blog: <a href="//www.die-katze.net">Aufstehen</a></h3>
        </li>
        <li>
          <h3>GitHub: <a href="//github.com/umigit">umigit</a></h3>
        </li>
        <li class="link-item">
          <h3><a></a></h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<style>
.link-card {
  width: 480px;
  height: 270px;
  background-color: #eee;
  position: relative;
  z-index: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.link-list {
  list-style: none;
  text-align: left;
  padding: 0;
}

.link-item {
  margin-bottom: 15px;
}

a {
  color: #000;
}

@media screen and (max-width: 479px) {
  .link-card {
    width: 320px;
    height: 180px;
  }
}
</style>
