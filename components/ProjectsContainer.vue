<template>
  <div class="containers">
    <div class="project-container" v-for="item in itemList" :key="item.name">
      <div class="skill-tags">
        <span class="tag-item" v-for="tag in item.skills" :key="tag">{{tag}}</span>
      </div>
      <p class="project-name">{{item.name}}</p>
      <div class="project-description">
        <label>重点与难点：</label>
        <p>{{item.resolve}}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ProjectContainer',
    props: {
      itemList: {
        type: Array,
        default: ()=>[]
      }
    }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .containers{
    .project-container{
      &:not(:last-child){
        margin-bottom: 30px;
      }
    }
  }
  .project-container{
    position: relative;
    .project-name{
      @include Height(22px);
      font-size: 14px;
      margin-bottom: 15px;
      font-weight:bold;
    }
    .skill-tags{
      position: absolute;
      top: 0;
      right: 20px;
      .tag-item{
        text-align: center;
        display: inline-block;
        min-width: 50px;
        padding-left: 2px;
        padding-right: 2px;
        border-radius: 4px;
        border: $mainColor solid 1px;
        color: $mainColor;
        margin-left: 6px;
        font-size: 12px;
      }
    }
    .project-description{
      /*width: 600px;*/
      font-size: 12px;
      width: 80%;
      margin-top: 10px;
      line-height: 1.5;
      > label {
        float: left;
        // display: block;
      }
      > p {
        line-height: 1.5;
        overflow: hidden;
      }
    }
  }
</style>
