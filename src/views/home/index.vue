<template>
  <div class="home">
    <div class="timeline">
      <h1>Home</h1>

      <br />
      <br />

      <Post />

      <br />
      <br />
      <br />
    </div>

    <div class="sidebar">
      <Avatar :size="80"/>
      <p>Ahmet Karslı</p>
    </div>
  </div>
</template>

<script>
import Avatar from "@/components/Avatar.vue";
import Post from "@/components/Post.vue";
export default {
  name: 'Home',
  components: {
    Post,
    Avatar,
  }
}
</script>

<style scoped>
.home {
  max-width: 605px;
  margin-left: auto;
  margin-right: auto;

  @media (min-width: 980px) {
    max-width: none;
    display: grid;
    grid-template-columns: 1fr 295px;
    grid-gap: 30px;
  }
}

.sidebar {
  display: none;
  @media (min-width: 980px) {
    display: block;
  }
}
</style>
