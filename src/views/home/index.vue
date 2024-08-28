<template>
  <div class="home">

    <div class="timeline">
      <h1>Home</h1>
      <Avatar :size="80"/>
    </div>

    <div class="sidebar">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed nonne merninisti licere mihi ista probare, quae sunt a te dicta? Refert tamen, quo modo. Quod ea non occurrentia fingunt, vincunt Aristonem; Duo Reges: constructio interrete. Quae cum dixisset paulumque institisset, Quid est?
      </p>
    </div>
  </div>
</template>

<script>
import Avatar from "@/components/Avatar.vue";
export default {
  name: 'Home',
  components: {
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
