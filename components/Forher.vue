<template>
    <div class="container-fluid forHerWrapper">
        <div class="col-12">
            <div class="row align-content-end">
                <div class="col-6 col-md-5">
                </div>
                <div class="col-6 col-md-7 px-0">
                    <div class="missionWrapper">
                        <img src="~/assets/images/forHerContent.jpg" width="100%" alt="">
                        <div class="missionDescription">{{desc}}</div>
                    </div>
                </div>
            </div>
            
            <div class="row btn-row">
                <div class="col-md-7 offset-md-5">
                    <button type="button" class="btn btn-light">For her</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: ['desc'],
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
.forHerWrapper {
    background-image: url(~/assets/images/forHerBg.png);
    background-size: cover;
    padding-bottom: 50px;
    background-position: center;
}

.missionWrapper {
    position: relative;

    .missionDescription {
        position: absolute;
        left: 10%;
        top: 0;
        bottom: 0;
        width: 30%;
        font-size: 40px;
        display: flex;
        align-items: center;
        color: #fff;
    }
}

.btn-row {
    transform: translateY(-50%);

    .btn {
        transform: translateX(-70%);
        font-size: 32px;
        border-radius: 35px;
        padding: 2px 40px;
    }
}
</style>