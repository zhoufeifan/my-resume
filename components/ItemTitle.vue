<template>
  <div class="handle-content">
    <div class="resume-item-head">
      <div class="resume-item-title">
        <img :src="icon"/>
        {{title}}
      </div>
    </div>
    <div class="content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ItemTitle',
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
  .handle-content{
    .resume-item-head{
      border-bottom: 1px $mainColor solid;
      margin-bottom: 10px;
      .resume-item-title{
        width: 140px;
        @include Height(40px);
        background-color: $mainColor;
        border-radius: 4px 4px 0 0 ;
        color: #ffffff;
        font-size: 18px;
        font-weight: 700;
        padding-left: 10px;
      }
    }
    .content{
      padding-left: 14px;
    }
    margin-bottom: 20px;
  }
</style>
