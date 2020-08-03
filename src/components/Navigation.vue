<template>
<div class='root'>
  <div class="container">
    <div class="row">
      <div class="col-3 no-padding">
      </div>
      <div class="col-6  no-padding">
        <img src='https://cdn.shopify.com/s/files/1/0313/2532/3401/files/RUX-Logo-OFFRED_x60.png' />
      </div>
      <div class="col-3  no-padding my-rux">
        <div class='text' @click='showRuxList=!showRuxList'>
          My Rux (5) <i v-if='!showRuxList' class="material-icons">expand_more</i><i v-else class="material-icons">expand_less</i>
        </div>
      </div>
    </div>
  </div>
  <div class="row">
    <div class="col-3">
    </div>
    <div class="col-9">
      <NavigationRuxList v-if='showRuxList' />
    </div>
  </div>

</div>
</template>
<script>
import NavigationRuxList from './NavigationRuxList.vue'
export default {
  name: 'Navigation',
  components: {
    NavigationRuxList
  },
  data: () => {
    return {
      showRuxList: false
    }
  }
}
</script>
<style lang='scss' scoped>
div.container {
    background-color: rgb(247,247,247);
    min-height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: none;

}
div.row {
    .no-padding {
        padding-left: 0;
        padding-right: 0;
    }
    width: 100%;
    .my-rux {
        display: flex;
        align-items: center;
        justify-content: center;
        .text {
            border-bottom: 1px solid;
            padding: 4px;
            cursor: pointer;
            font-size: 13px;
            text-transform: uppercase;
            .material-icons {
                position: relative;
                top: 7px;
            }
        }
    }
}
</style>
