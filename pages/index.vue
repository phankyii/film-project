<template>
  <div>
     <!-- headers -->
           <Header></Header>
    <!-- end headers -->
    <!-- barners -->
          <Barner></Barner>
     <!-- end barner -->
     <!-- content -->
          <Contents></Contents>
    <!-- end content -->
          <!-- footers -->
       <Footer></Footer>
          <!-- end footer -->
  </div>
</template>

<script>
// import Tutorial from '@/components/Tutorial.vue'
import Header from "@/components/Header.vue";
import Barner from '@/components/Barner.vue';
import Contents from '@/components/Contents.vue';
import Footer from "@/components/Footer.vue";
export default {
  name: "IndexPage",
  
  components:  {
    Header,
    Barner,
    Contents,
    Footer
  }
};
</script>
