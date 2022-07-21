<template>
  <div class="abc-wrapper">
    <div v-for="item in users" :key="item.cmnd" class="item">
      <p :class="item.class ? 'color-' + item.class : ''">{{ item.name }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "abc",

  props: {
    usersArray: {
      type: Array,
      default: () => [],
    },
  },

  data() {
    return {
      users: [
        { name: "vin", cmnd: 1234, class: "red" },
        { name: "ky", cmnd: 7492, class: "blue" },
        { name: "nguyen", cmnd: 43345 },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.color-red {
  color: red;
}
.color-blue {
  color: blue;
}
.abc-wrapper {
  display: flex;
  .item {
    height: 200px;
    width: 100px;
    background-color: gray;
    color: white;
  }
}
</style>
