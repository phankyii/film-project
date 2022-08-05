<template>
  <div>
    <VueSlickCarousel
      v-bind="setting"
      :arrows="true"
      :dots="true"
      class="slick"
    >
      <!-- <div v-if="sliderShow.length" > -->

      <div v-for="(slider, index) in sliderShow" :key="'item' + index">
        <div class="show">
          <img :src="slider.url" alt="" />
          <div class="text-slider">
            <h1>{{ slider.text }}</h1>
            <h2>{{slider.heading}}</h2>
            <p>{{slider.para}}</p>
            <a :href="slider.anchor">Watch Trailer</a>
          </div>
        </div>
      </div>

      <!-- </div> -->
    </VueSlickCarousel>
  </div>
</template>
 
<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "Slider",
  components: { VueSlickCarousel },
  data() {
    return {
      setting: {
        arrows: false,
        dots: true,
        infinite: true,
        slidesToShow: 1,
        slidesToScroll: 1,
        autoplay: true,
        speed: 500,
        autoplaySpeed: 1500,
        cssEase: "linear",
      },
      sliderShow: [
        {
          text: "Commedy",
          url: "http://themescare.com/demos/filmoja-view/assets/img/slider-1.jpeg",
          heading: "Sunriser : Fury 2019",
          para:"Realease On: 20 Dec,2014",
          anchor:"https://www.youtube.com/watch?v=1Q8fG0TtVAY"
        },
        {
          text: "Action",
          url: "http://themescare.com/demos/filmoja-view/assets/img/slider-2.jpeg",
          heading: "Daring Joker : Car",
          para:"Realease On: 20 Dec,2014",
          anchor:"https://www.youtube.com/watch?v=1Q8fG0TtVAY"
        },
        {
          text: "Science Fiction",
          url: "http://themescare.com/demos/filmoja-view/assets/img/slider-4.jpeg",
          heading: "Black Stone Of The Club",
          para:"Realease On: 20 Dec,2014",
          anchor:"https://www.youtube.com/watch?v=1Q8fG0TtVAY"
        },
      ],
    };
  },
};
</script> 

