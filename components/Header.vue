<template>
  <b-navbar toggleable class="navbar-bg">
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
</template>

<script>
</script>

<style lang="scss" scoped>
.navbar-bg {
    background: #EBE4D8;
}

.navbar-logo {
    height: 40px;
    img {
        height: 25px;
        object-fit: contain;
        margin-right: 10px;
    }
    span {
        padding-top: 5px;
    }
}
</style>