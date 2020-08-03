<template>
  <div class="root">
    <div class="item">
      <i class="material-icons col-2">face</i>
      <span class="col-10 label">Andrew Winter Outerwear</span>
    </div>
    <div class="item">
      <i class="material-icons col-2">face</i>
      <span class="col-10 label">Jackie Winter Outerwear</span>
    </div>
    <div class="item">
      <i class="material-icons col-2">face</i>
      <span class="col-10 label">this is way to much text to fit properly</span>
    </div>
    <div class="item">
      <i class="material-icons col-2">face</i>
      <span class="col-10 label">Andrew Winter Tech Gear</span>
    </div>
    <div class="item">
      <i class="material-icons col-2">face</i>
      <span class="col-10 label">less text</span>
    </div>
    <div class="item">
      <span class="see-all">See All</span>
    </div>
  </div>
</template>
<script>
export default {
  name: "NavigationRuxList"
};
</script>
<style lang='scss' scoped>
.root {
  position: absolute;
  right: 0px;
  display: block;
  background-color: rgb(247, 247, 247);
  padding-left: 8px;
  padding-right: 8px;
  .item {
    border-bottom: solid 1px white;
    padding: 8px;
    display: flex;
    cursor: pointer;
    .label {
      text-align: left;
    }
    .see-all {
      text-align: center;
      width: 100%;
    }
    span {
      &:hover {
        color: #aaa;
      }
    }
  }
}
</style>
