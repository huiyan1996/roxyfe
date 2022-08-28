<template>
    <div class="missionWrapper px-3 py-5 mobileView">
        <b-row align-v="start" class="justify-content-center">
            <b-col class="missionDesc" cols="6">
                <p class="pt-3 pl-3">{{desc}}</p>
            </b-col>
            <b-col class="missionImg" cols="6" lg="4">
                <img class="missionImgBg" src="~/assets/images/mission.png" alt="Mission" />
            </b-col>
        </b-row>
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
.missionWrapper {
    background: #FDDFDA;
    
    .missionImg {
        position: relative;
        
        .missionImgBg {
            width: 100%;
            object-fit: cover;
            border-radius: 150px 150px 0 0;
            opacity: 0.8;
        }
    }

    .missionDesc {
        font-size: 16px;
        line-height: 16px;
    }
}
</style>