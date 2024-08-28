<template>
<figure class="avatar">
  <img src="@/assets/avatar.jpg" :alt="alt" :width="size" :height="size">
</figure>
</template>

<script>

export default {
  name: "Avatar",
  props: {
    alt: {
      type: String,
    },
    size: {
      type: Number
    }
  }
};

</script>

<style scoped>
.avatar {
  display: inline-flex;
  padding: 2px;
  border-radius: 999px;
  background: linear-gradient(219deg, rgba(184,63,140,1) 0%, rgba(237,158,90,1) 100%);

  img {
  border-radius: inherit;
  border: 2px solid white;
  }
}

</style>