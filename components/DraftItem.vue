<template>
  <div class="draft-group-item">
    <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
  </div>
</template>

<script>
  export default {
    name: 'DraftItem',
    props: {
      title: String,
      icon: String,
    },
    data(){
      return {
      };
    }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .draft-group-item{
    position: relative;
    padding: 10px 0 10px 20px;
    font-size: 14px;
    z-index: 2;
    &::before{
      position: absolute;
      content: " ";
      top: 4px;
      left: -4px;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      z-index: 5;
      background-color: $mainColor;
    }
    &::after{
      position: absolute;
      content: " ";
      top: 0;
      left: -8px;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      opacity: .5;
      z-index: 4;
      background-color: $mainColor;
    }
  }
</style>
