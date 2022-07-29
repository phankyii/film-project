<template>
  <li class=header-item>
    <a href="">{{data.text}}</a>
    <ul class="header-item-child">
      <HeaderItem v-for="(item, index) in data.child" :key="'child'+index" :data="item" ></HeaderItem>
    </ul>
   <i  v-if="data.child.length"
      class="fa fa-caret-right" 
      aria-hidden="true"></i>
  </li>
</template>

<script>

import HeaderItem from "@/components/HeaderItem";

export default {
  name: "HeaderItem",
  components: {
    HeaderItem,
  },
  props:{
    data:{
      type: Object,
      default: ()=> {},
    }
  }

  
};
</script>
