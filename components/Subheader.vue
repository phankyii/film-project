<template>
  <div class="sub-header">
      <div class="all-sub-header">
    <div class="sub-header-left">
      <div
        v-for="(item, index) in subHeader"
        :key="'child' + index"
        v-html="item.icon"
      ></div>
    </div>
    <div class="sub-header-right">
        <div v-for="(child,index) in textHeader" :key="'item' + index" >
           <a href="">{{child.text}}</a> 
        </div>
        </div>
        </div>
  </div>
</template>
<script>
export default {
  name: "Subheader",

  data() {
    return {
      subHeader: [
        {
          icon: '<i class="fa fa-envelope" aria-hidden="true"></i>',
        },
        {
          icon: '<i class="fa fa-user-circle" aria-hidden="true"></i>',
        },
        {
          icon: ' <i class="fa fa-id-card" aria-hidden="true"></i>',
        },
        {
          icon: ' <i class="fa fa-bell" aria-hidden="true"></i>',
        },
        {
          icon: ' <i class="fa fa-tags" aria-hidden="true"></i>',
        },
      ],
      textHeader: [
        {
          text: "Community",
        },
        {
          text: "FAQ's",
        },
        {
          text: "Help",
        },
        {
          text: "Login",
        },
        {
          text: "Register",
        },
      ],
    };
  },
};
</script>
