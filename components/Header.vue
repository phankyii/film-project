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
          <li><a href="">Home</a></li>
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
          <li><a href="">Contact</a></li>
        </ul>
      </div>
    </div>
</template>


<script>
export default {
    name: "Header"
}
</script>