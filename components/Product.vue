<template>
    <div v-if="displayList" class="container-fluid productWrapper p-5">
        <b-row class="justify-content-center text-center">
            <b-col class="products mb-3" cols="12" sm="6" lg="4" v-for="(v, k) in displayList" :key="k">
                <img :src="require(`@/assets/images/${v.src}`)" :alt="v.title">
                <div class="productTitle">{{v.title}}</div>
            </b-col>
        </b-row>
    </div>
</template>

<script>
export default {
  name: 'IndexPage',
  props: ['list'],
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
.productWrapper {
    display: flex;
    width: 100%;
    background: #ffffff;
    color: #414040;

    .products {
        width: 100%;
        img {
            width: 100%;
            object-fit: contain;
        }
    }
}
</style>