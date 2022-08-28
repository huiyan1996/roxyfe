<template>
    <div class="container-fluid missionWrapper p-5">
        <b-row class="mb-5" align-content="end">
            <b-col cols="6" md="5">
                <!-- <div class="missionDescription">{{desc}}</div> -->
            </b-col>
            <b-col class="for-her" cols="6" md="7">
                <!-- <img class="missionImg" src="~/assets/images/marian-luzi-DBeaZsvTKIw-unsplash.jpg" alt=""> -->
                <div class="missionDescription">{{desc}}</div>
            </b-col>
        </b-row>
        <b-row class="btn-row">
            <b-col class="text-center" cols="12">
                <button type="button" class="btn btn-light">For her</button>
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

    .for-her {
        background-image: url("~/assets/images/marian-luzi-DBeaZsvTKIw-unsplash.jpg");
        background-size: cover;
        height: 420px;
    }

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

        .btn {
            font-size: 32px;
            border-radius: 35px;
            padding: 2px 40px;
        }
    }
}
</style>