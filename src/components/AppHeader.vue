<script>
export default {
  data() {
    return {
        navItems: [
        {
          navTitle: "CHARACTERS",
        },
        {
          navTitle: "COMICS",
        },
        {
          navTitle: "MOVIES",
        },
        {
          navTitle: "TV",
        },
        {
          navTitle: "GAMES",
        },
        {
          navTitle: "COLLECTIBLES",
        },
        {
          navTitle: "VIDEOS",
        },
        {
          navTitle: "FANS",
        },
        {
          navTitle: "NEWS",
        },
        {
          navTitle: "SHOP",
        },
      ],
    };
  },
};
</script>

<template>
<header>
    <div class="large-container">
        <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="Logo DC Comics" />
        </div>
        <nav>
        <ul>
            <li v-for="item in navItems" :key="item.navTitle">
            <a href="">{{ item.navTitle }}</a>
            </li>
        </ul>
        </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
  padding: 1rem;
  background-color: $white;
  @include flex();
  z-index: 999;
  .logo {
    img {
      width: 80px;
    }
  }

  ul {
    @include flex();
    list-style: none;
    gap: 1rem;

    a {
    text-decoration: none;
    color: $header-color;
    }
  }
}
</style>