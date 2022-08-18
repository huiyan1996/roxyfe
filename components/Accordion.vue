<template>
  <div v-if="displayList" class="container-fluid px-0 mb-5">

    <h1 class="text-center my-3">{{title}}</h1>

    <div class="container">
        <div class="accordionWrapper" v-for="(v, k) in displayList" :key="k">
            <button type="button" class="accordionTitle" :class="{open: v.isShow}" @click="v.isShow = !v.isShow">
                <div class="titleWidth">
                    <span>{{v.title}}</span>
                    <b-icon class="icon" :icon="v.isShow?'dash-lg':'plus-lg'"></b-icon>
                </div>
            </button>
            <b-collapse v-model="v.isShow">
                <div class="accordionContent" v-html="v.content"></div>
            </b-collapse>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: ['list', 'title'],
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
                  content: v['content'],
                  isShow: false,
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