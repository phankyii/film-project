<template>
  <li class="header-item">
    <a href="">{{ data.text }}</a>
    <ul class="header-item-children">
        <HeaderItem v-for="item, index in data.children" :key="'children' + index" :data="item"></HeaderItem>
    </ul>
    <i
      v-if="data.children.length"
      class="fa fa-caret-right"
      aria-hidden="true"
    ></i>
  </li>
</template>

<script>
import HeaderItem from "@/components/HeaderItem.vue";

export default {
  name: "HeaderItem",

  components: {
    HeaderItem
  },

  props: {
    data: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
