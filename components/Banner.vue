<template>
    <div class="container-fluid bannerWrapper p-5">
        <b-row class="bannerVid mb-5">
            <b-col cols="12">
                <img src="~/assets/images/josue-michel-wtGp_v9VhqM-unsplash.jpg" alt="">
            </b-col>
        </b-row>
    </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: [],
  data() {
    return {
        displayList: null,
        visible: true,
    }
  },
  methods: {
  },
  mounted() {
  }
}
</script>

<style lang="scss" scoped>
.bannerWrapper {
    background: #FCE7E3;
    color: #414040;

    .bannerVid {
        width: 100%;

        img, video {
            width: 100%;
        }
    }
}
</style>