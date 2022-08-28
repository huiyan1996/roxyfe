<template>
  <div class="aboutWrapper p-5">
    <div class="container">
        <b-row class="justify-content-center">
            <b-col cols="10">
                <b-row align-v="end">
                    <b-col class="aboutImg" cols="5" lg="4">
                        <img class="aboutImgBg" src="~/assets/images/vasilina-sirotina-Qwf-Y9MjED8-unsplash.jpg" alt="About Us" />
                        <img class="aboutRose" src="~/assets/images/rose.png" alt="Rose" />
                    </b-col>
                    <b-col class="aboutDesc" cols="7">
                        <h1 class="">About Us</h1>
                        <p class="pl-5">{{desc}}</p>
                    </b-col>
                </b-row>
            </b-col>
        </b-row>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
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
.aboutWrapper {
    background: #EBE4D8;
    
    .aboutImg {
        position: relative;
        
        .aboutImgBg {
            width: 100%;
            object-fit: cover;
            border-radius: 150px 150px 0 0;
            opacity: 0.8;
        }

        .aboutRose {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            height: 50px;
            width: 50px;
            filter: invert(1);
        }
    }

    .aboutDesc {
        font-size: 20px;
        
        h1 {
            font-weight: bold;
        }
    }
}
</style>