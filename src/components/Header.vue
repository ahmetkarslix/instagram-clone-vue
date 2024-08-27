<template>
  <header class="header">
    <container class="header-inner">
    <router-link class="logo" to="/">
      Instagram
    </router-link>

    <form class="search">
      <input type="text" placeholder="Search" />
    </form>

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
      <router-link to="/profile">Profile
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
export default {
  name: "MainHeader",
  components: {
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
  border-bottom: 1px solid #dbdbdb;
}

.header-inner {
  height: 60px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  align-items: center;
}

.logo {
  font-size: 1.6rem;
  font-weight: bold;
}

.search {
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
.navigation {
  display: flex;
  justify-content: flex-end;
  align-items: center;

  a {
    margin-left: 20px;
    color: #262626;
  }
}


</style>