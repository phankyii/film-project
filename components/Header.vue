<template>
  <div class="header">
    <div class="header-left">
      <img class="pd15" src="@/assets/image/logo.png" alt="" />
      <div class="input pd15">
        <input type="text" name="" required id="" placeholder="Search..." />
        <div class="search">
          <i class="fa fa-search" aria-hidden="true"></i>
        </div>
      </div>
    </div>
    <div class="header-right">
      <ul class="pd15">
        <li
          v-for="(menu, index) in menuPageList"
          :key="'parent' + index"
          class="same"
        >
          <a href="">{{ menu.text }}</a>
          <!-- renderchilren -->
          <ul v-if="menu.children.length" class="sub-same">
            <HeaderItem
              v-for="(item, index) in menu.children"
              :key="'menu' + index"
              :data="item"
            ></HeaderItem>
          </ul>
        </li>

        <!-- <li>
          <a href="">{{ name }}</a>
        </li>
        <li class="same">
          <a href="">Pages</a>
          <ul class="sub-same">
            <li><a href="">About Us</a></li>
            <li><a href="">Pricing</a></li>
            <li>
              <a href="">Blog</a>
              <ul class="child-pages1">
                <li><a href="">Blog</a></li>
                <li><a href="">Blog Details</a></li>
              </ul>
              <i class="fa fa-caret-right" aria-hidden="true"></i>
            </li>
            <li>
              <a href="">Authentication</a>
              <ul class="child-pages2">
                <li><a href="">Login</a></li>
                <li><a href="">Register</a></li>
              </ul>
              <i class="fa fa-caret-right" aria-hidden="true"></i>
            </li>
            <li><a href="">404 Error</a></li>
          </ul>
        </li>
        <li class="same">
          <a href="">Movies</a>
          <ul class="sub-same">
            <li><a href="">Movies List Sidebar</a></li>
            <li>
              <a href="">Movies Grid</a>
              <ul class="child-movies">
                <li><a href="">Grid Sidebar</a></li>
                <li><a href="">Full Page Grid</a></li>
              </ul>
              <i class="fa fa-caret-right" aria-hidden="true"></i>
            </li>
            <li><a href="">Movies Details</a></li>
          </ul>
        </li>
        <li class="same">
          <a href="">Tv Show</a>
          <ul class="sub-same">
            <li><a href="">Tv Series</a></li>
            <li><a href="">Series Details</a></li>
          </ul>
        </li>
        <li class="same">
          <a href="">Celebrities</a>
          <ul class="sub-same">
            <li><a href="">All Celebrities</a></li>
            <li><a href="">Celebrities Details</a></li>
          </ul>
        </li>
        <li><a href="">Contact</a></li> -->
      </ul>
    </div>
  </div>
</template>

<script>
import HeaderItem from "@/components/HeaderItem.vue";

export default {
  name: "Header",

  components: {
    HeaderItem,
  },

  // dùng để truyền từ cha vào
  props: {
    name: {
      type: String,
      default: () => "Home",
    },
  },

  // chỉ có tác dụng ở trong này thôi
  data() {
    return {
      menuPageList: [
        {
          text: "Home",
          url: "/",
          children: [],
        },
        {
          text: "Pages",
          url: "/",
          children: [
            { text: "About us", url: "/", children: [] },
            { text: "Pricing", url: "/", children: [] },
            {
              text: "Blog",
              url: "/",
              children: [
                { text: "Blog", url: "/", children: [] },
                { text: "Blog Details", url: "/", children: [] },
              ],
            },
            {
              text: "Authentication",
              url: "/",
              children: [
                { text: "Authentication 2", url: "/", children: [] },
                { text: "Authentication 3", url: "/", children: [] },
              ],
            },
            {
              text: "404",
              url: "/",
              children: [
                { text: "Blog", url: "/", children: [
                { text: "404 1", url: "/", children: [] },
                { text: "404 2", url: "/", children: [] },
                ] },
                { text: "Blog Details", url: "/", children: [] },
              ],
            },
          ],
        },
      ],
    };
  },
};
</script>
