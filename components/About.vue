<template>
  <div class="container-fluid px-0 mb-5">
    <div class="container">
        <div class="aboutWrapper" >
            <div class="col-lg-3">
                <img src="~/assets/images/vasilina-sirotina-Qwf-Y9MjED8-unsplash.jpg" alt="About Us">
            </div>
            <div class="col-lg-7">
                <h1 class="text-center my-3">{{title}}</h1>
                <p>{{aboutDesc}}</p>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  props: ['aboutDesc', 'title'],
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
.accordionWrapper {
    margin-bottom: 20px;

    .accordionTitle {
        background: var(--lightGrey);
        color: var(--blue);
        border: none;
        width: 100%;
        padding: 15px;
        text-align: left;
        font-weight: bold;
        transition: .3s;

        .titleWidth {
            display: flex;
            width: 85%;
            margin: 0 auto;
            justify-content: space-between;
            align-items: center;

            .icon {
                font-size: 15px;
            }
        }

        &.open {
            background: var(--blue);
            color: #fff;
        }
    }

    .accordionContent {
        padding: 30px 7.5%;
        box-shadow: 0 0 15px -10px #000;
        transition: .3s;
        background: #fff;
    }
}
</style>