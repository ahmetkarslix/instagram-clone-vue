<template>
  <div class="home">
    <h1>This is an Home page</h1>
    <custom-text class="a1" tag="p">Merhaba Dünya</custom-text>
    <custom-text class="a2" tag="p" size="small">Merhaba Dünya</custom-text>
    <custom-text class="a3" tag="p" size="xsmall">Merhaba Dünya</custom-text>
    <custom-text class="a4" tag="p" size="xxsmall">Merhaba Dünya</custom-text>


  </div>
</template>

<script>
import CustomText from '@/components/CustomText.vue'
export default {
  name: 'Home',
  components: {
    CustomText,
  }
}
</script>

<style>
.a1 {
  color: #ED4956;
}
.a2 {
  color: #FAFAFA;
}
.a3 {
  color: #DBDBDB;
}
.a4 {
  color: #C7C7C7;
}
</style>
