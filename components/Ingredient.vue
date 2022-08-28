<template>
    <div v-if="displayList" class="ingredientWrapper p-5 mobileView">
        <b-row class="justify-content-center">
            <b-col class="ingredients" cols="12" md="4" v-for="(v, k) in displayList" :key="k">
                <p>{{v.content}}</p>
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
                  content: v['content'],
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
.ingredientWrapper {
    background: #FACBC6;
    color: #414040;

    .ingredients {
        text-align: center;
    }
}

@media only screen and (max-width: 768px) {
    .ingredients {
        margin: 20px 0px;
    }
    .ingredients:nth-child(odd) {
        padding-left: 50px;
        text-align: left!important;
    }
    .ingredients:nth-child(even) {
        padding-right: 50px;
        text-align: right!important;;
    }
}
</style>