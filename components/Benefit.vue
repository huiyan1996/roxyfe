<template>
    <div class="container-fluid benefitWrapper p-5">
        <b-row class="mb-5">
            <b-col cols="6" md="3" offset-md="3">
                <img class="benefitImg" src="~/assets/images/vasilina-sirotina-Qwf-Y9MjED8-unsplash.jpg" alt="">
            </b-col>
            <b-col cols="6" md="3">
                <h2>Serum</h2>
                <div class="benefitDescription">{{desc}}</div>
            </b-col>
        </b-row>
        <b-row v-if="displayList">
            <b-col cols="6" md="3" v-for="(v, k) in displayList" :key="k">
                <div class="benefits">
                    <img :src="require(`@/assets/images/${v.src}`)" :alt="v.title" />
                    <div class="benefitTitle text-center">{{v.title}}</div>
                </div>
            </b-col>
        </b-row>
    </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: ['desc', 'list'],
  data() {
    return {
        displayList: null,
        visible: true,
    }
  },
  methods: {
      rebuildList() {
          let newList = [];
          this.list.forEach(function(v,k){
              newList.push({
                  title: v['title'],
                  src: v['src'],
              });
          });

          this.displayList = newList;
      }
  },
  mounted() {
      this.rebuildList();
  }
}
</script>

<style lang="scss" scoped>
.benefitWrapper {
    background: #FCE7E3;
    color: #414040;

    .benefitImg {
        width: 100%;
        object-fit: contain;
        border-radius: 35%;
    }

    .benefitDescription {
        margin-top: 15px;
        font-size: 12px;
    }

    .benefits {
        width: 100%;
        img {
            width: 100%;
            object-fit: contain;
        }
        .benefitTitle {
            font-weight: bold;
        }
    }
}
</style>