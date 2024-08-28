<template>
  <header class="header">
    <container class="header-inner">
      <!-- Logo -->
    <router-link class="logo" to="/">
      Instagram
    </router-link>

    <!-- Search -->
    <form class="search">
      <input type="text" placeholder="Search" />
    </form>

    <!-- Navigation -->
    <nav class="navigation">
      <router-link to="/">
      <HomeFill v-if="$route.name === 'Home'"/>
      <Home v-else />
      </router-link>
      <router-link to="/direct">
      <DirectFill v-if="$route.name === 'Direct'"/>
      <Direct v-else />
      </router-link>
      <router-link to="/explore">
      <ExploreFill v-if="$route.name === 'Explore'"/>
      <Explore v-else />
      </router-link>
      <router-link to="/profile">
        <Avatar size="26" />
      </router-link>
    </nav>
    </container>
  </header>
</template>

<script>
import Home from "@/icons/Home.vue";
import HomeFill from "@/icons/HomeFill.vue";
import Direct from "@/icons/Direct.vue";
import DirectFill from "@/icons/DirectFill.vue"
import Explore from "@/icons/Explore.vue";
import ExploreFill from "@/icons/ExploreFill.vue";
import Container from "@/components/Container.vue";
import Avatar from "@/components/Avatar.vue";
export default {
  name: "MainHeader",
  components: {
    Avatar,
    Container,
    Home,
    HomeFill,
    Direct,
    DirectFill,
    Explore,
    ExploreFill
  }
}
</script>

<style scoped>
.header {
  z-index: 90;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  background-color: white;
  border-bottom: 1px solid #dbdbdb;
}

.header-inner {
  height: var(--header-height);
  display:flex;
  align-items: center;
  justify-content: center;

  @media (min-width: 980px) {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
  }
}

.logo {
  font-size: 1.6rem;
  font-weight: bold;
}

.search {
  display: none;
  @media(min-width: 980px) {
    display: block;
    text-align: center;

    input {
      width: 215px;
      height: 28px;
      border: 1px solid #dbdbdb;
      border-radius: 3px;
      background-color: #FAFAFA;
      padding-left: 20px;
      padding-right: 20px;
    }
  }
}
.navigation {
  z-index: 90;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: white;
  border-top: 1px solid #dbdbdb;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-around;


  @media (min-width: 980px) {
    height:auto;
    border: 0;
    position: static;
    justify-content: flex-end;

    a {
      margin-left: 20px;
      color: #262626;
    }
  }
}


</style>