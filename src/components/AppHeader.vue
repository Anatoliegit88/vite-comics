<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menuList: [
        {
          title: "CHARACTERS",
          url: "/characters",
          active: false,
        },
        {
          title: "COMICS",
          url: "/comics",
          active: true,
        },
        {
          title: "MOVIES",
          url: "/movies",
          active: false,
        },
        {
          title: "TV",
          url: "/tv",
          active: false,
        },
        {
          title: "GAMES",
          url: "/games",
          active: false,
        },
        {
          title: "COLLECTIBLES",
          url: "/collectibles",
          active: false,
        },
        {
          title: "VIDEOS",
          url: "/videos",
          active: false,
        },
        {
          title: "FANS",
          url: "/fans",
          active: false,
        },
        {
          title: "NEWS",
          url: "/news",
          active: false,
        },
        {
          title: "SHOP",
          url: "/shop",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="logo">
      <a href="">
        <img src="../assets/img/dc-logo-bg.png" alt="" />
      </a>
    </div>
    <div class="menuList">
      <div class="navbar">
        <ul>
          <li v-for="(link, index) in menuList" :key="index">
            <a :class="{ active: link.active }" :href="link.url">{{
              link.title
            }}</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@use "../styles/general.scss" as *;
</style>
