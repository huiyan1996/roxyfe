<template>
    <div class="container-fluid missionWrapper p-5">
        <b-row class="mb-5">
            <b-col cols="6" md="3" offset-md="3">
                <div class="missionDescription">{{desc}}</div>
            </b-col>
            <b-col cols="6" md="3">
                <img class="missionImg" src="~/assets/images/vasilina-sirotina-Qwf-Y9MjED8-unsplash.jpg" alt="">
            </b-col>
        </b-row>
        <b-row class="btn-row">
            <b-col class="text-center" cols="12">
                <button type="button" class="btn btn-light">For Her</button>
            </b-col>
        </b-row>
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
.missionWrapper {
    background: #FCE7E3;
    color: #414040;

    .missionImg {
        width: 100%;
        object-fit: contain;
        border-radius: 40% 40% 0% 0%;
    }

    .missionDescription {
        margin-top: 15px;
        font-size: 16px;
    }

    .btn-row {
        margin-top: -50px;
    }
}
</style>