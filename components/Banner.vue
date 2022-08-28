<template>
    <div class="bannerWrapper mobileView">
        <div class="col-12">
            <div class="row">
                <b-col class="bannerImg px-0" cols="12">
                    <img class="bannerImgBg" src="~/assets/images/roxyLandingBg.png" alt="Mobile Banner">
                    <img class="bannerRose" src="~/assets/images/rose.png" alt="Rose" />
                </b-col>
            </div>
        </div>
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
    width: 100%;
    background: #FCE7E3;
    color: #414040;

    .bannerImg {
        position: relative;
        
        .bannerImgBg {
            width: 100%;
            object-fit: cover;
            opacity: 0.8;
        }

        .bannerRose {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            height: 50px;
            width: 50px;
            filter: invert(1);
        }
    }
}
</style>