<template>
    <div class="container-fluid benefitWrapper p-5">
        <div class="benefitContainer">
            <b-row class="justify-content-center mb-5">
                <b-col md="10" lg="8">
                    <b-row>
                        <b-col cols="6" md="3">
                            <img class="benefitImg" src="~/assets/images/vasilina-sirotina-Qwf-Y9MjED8-unsplash.jpg" alt=""></img>
                        </b-col>
                        <b-col cols="6" offset-md="1">
                            <div class="benefitContent">
                                <h2>Serum</h2>
                                <div class="benefitDescription">{{desc}}</div>
                            </div>
                        </b-col>
                    </b-row>
                </b-col>
            </b-row>
        </div>
            <b-row v-if="displayList" class="justify-content-center">
                <b-col md="10" lg="8">
                    <b-row>
                        <b-col cols="6" md="3" v-for="(v, k) in displayList" :key="k">
                            <div class="benefits">
                                <img :src="require(`@/assets/images/${v.src}`)" :alt="v.title" />
                                <div class="benefitTitle text-center">{{v.title}}</div>
                            </div>
                        </b-col>
                    </b-row>
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

    .benefitContainer {
        position: relative;
        
        &::before {
            content: "";
            position: absolute;
            top: 30%;
            transform: translateY(-50%);
            left: 0px;
            right: 0px;
            height: 1.5px;
            background: #666;
        }
    }

    .benefitImg {
        width: 100%;
        object-fit: contain;
        // clip-path: ellipse(40% 48% at 50% 50%);
        border-radius: 120px;
    }

    .benefitContent {
        // margin-top: 30%;
        position: relative;
        top: calc(30% + 20px);
    }

    .benefitDescription {
        background: #FCE7E3;
        margin-top: 15px;
        font-size: 16px;
    }

    .benefits {
        width: 100%;
        img {
            width: 100%;
            object-fit: contain;
            border-radius: 50%;
        }
        .benefitTitle {
            font-weight: bold;
        }
    }
}
</style>