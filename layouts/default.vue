<template>
  <div>
    <Subheader></Subheader>
    <Header></Header>
    <div class="page-container">
      <Nuxt />
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Subheader from '@/components/Subheader.vue';
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";


export default {
  components: {
    Subheader,
    Header,
    Footer,
   
  },
};
</script>
<style scoped >
/* .page-container{
  margin-top: 86px;
} */
</style>