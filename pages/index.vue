<template>
  <div>
    <!-- <Infojs></Infojs> -->
    <Slider></Slider>
    <!-- <Barner></Barner> -->

    <Contents></Contents>
  </div>
</template>

<script>
// import Tutorial from '@/components/Tutorial.vue'
// import Barner from "@/components/Barner.vue";
// import Infojs from '@/components/Infojs.vue';
import Slider from "@/components/Slider.vue";
import Contents from "@/components/Contents.vue";

export default {
  name: "IndexPage",
  layout: "default",
  components: {
    // Barner,
    //  Infojs,
    Slider,
    Contents,
   
  },
};

</script>
