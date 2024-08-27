<template>
  <div class="app">
    <MasterHeader />

    <main class="main">
      <Container>
        <router-view />
      </Container>
    </main>


  </div>
</template>

<script>
import MasterHeader from "@/components/Header.vue";
import Container from "@/components/Container.vue";
export default {
  name: "App",
  components: {
    Container,
    MasterHeader
  }
}
</script>

<style scoped>
.main {
  margin-top: 40px;
}

</style>