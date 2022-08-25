<template>
  <div class="container-fluid">
    <div class="container navbar">
      <div class="logo mobileView"><img src="~/assets/images/rose.png" alt="Logo"><span>ROSYFOXY</span></div>

      <a href="javascript:;" class="menuIco mobileView" @click="expanded=!expanded">
        <b-icon v-if="expanded" icon="x-lg"></b-icon>
        <b-icon v-else icon="list"></b-icon>
      </a>

      <div class="overlay" v-if="expanded" @click="expanded=false"></div>
      <div class="menu" :class="{open: expanded}">
        <a href="#" class="menuItem">Home</a>
        <a href="#" class="menuItem">Product</a>
        <div class="logo pcView"><img src="~/assets/images/rose.png" alt="Logo"><span>ROSYFOXY</span></div>
        <a href="#" class="menuItem">Shop</a>
        <a href="#" class="menuItem">Contact</a>
      </div>
    </div>
    <!-- <b-navbar toggleable class="navbar-bg navbar-mobile">
      <b-navbar-brand class="navbar-logo" href="#"><img src="~/assets/images/rose.png" alt="Logo"><span>ROSYFOXY</span></b-navbar-brand>

      <b-navbar-toggle target="navbar-toggle-collapse">
        <template #default="{ expanded }">
          <b-icon v-if="expanded" icon="x-lg"></b-icon>
          <b-icon v-else icon="list"></b-icon>
        </template>
      </b-navbar-toggle>

      <b-collapse id="navbar-toggle-collapse" is-nav>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item href="#">Product</b-nav-item>
          <b-nav-item href="#">Shop</b-nav-item>
          <b-nav-item href="#">Contact</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    
    <b-navbar class="navbar-bg text-center navbar-web">
      <b-navbar-nav class="mr-auto">
          <b-nav-item href="#">Home</b-nav-item>
          <b-nav-item href="#">Product</b-nav-item>
        </b-navbar-nav>
        <b-navbar-brand class="navbar-logo" href="#">
          <img src="~/assets/images/rose.png" alt="Logo"><span>ROSYFOXY</span>
        </b-navbar-brand>
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">Shop</b-nav-item>
          <b-nav-item href="#">Contact</b-nav-item>
        </b-navbar-nav>
  </b-navbar> -->
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      expanded: false,
    }
  },
}
</script>

<style lang="scss" scoped>
// .navbar-mobile {
//   display: none;
// }
// .navbar-web {
//   display: flex;
// }

// .navbar-bg {
//     background: #EBE4D8;
// }

// .navbar-logo {
//     height: 40px;
//     img {
//         height: 25px;
//         object-fit: contain;
//         margin-right: 10px;
//     }
//     span {
//         padding-top: 5px;
//     }
// }

// .navbar-light .navbar-toggler {
//   border: none;
// }

// @media only screen and (max-width: 768px) {
//   .navbar-mobile {
//     display: flex;
//   }
//   .navbar-web {
//     display: none;
//   }
// }
</style>