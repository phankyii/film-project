<template>
  <div>
    <Header></Header>
    <div class="page-container">
      <Nuxt />
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    Header,
    Footer,
  },
};
</script>
<style scoped >
.page-container{
  margin-top: 86px;
}
</style>