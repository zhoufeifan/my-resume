<template>
  <div class="work-content-list">
    <div class="work-content" v-for="item in workList" :key="item.title">
      <p class="title">
        {{item.title}}
        <span class="skill">{{item.skill}}</span>
      </p>
      <p class="hint" v-if="item.desc">项目描述：{{item.desc}}</p>
      <p class="resolve" v-for="(s,index) in item.resolves" :key="index" v-html="s"></p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'CareerTitle',
    props: {
      workList: Array
    },
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .work-content-list{
    .work-content{
      margin-right: 10%;
      margin-top: 10px;
      .title {
        font-size: 12px;
        position: relative;
        &::after{
          content: '';
          display: block;
          width: 100%;
          height: 1px;
          background-color: #ccc;
          transform: scaleY(0.5);
        }
        // border-bottom: 1px solid #ccc;
        .skill{
          font-size: 10px;
          font-weight: 500;
          // float: right;
            margin-left: 30px;
          color: $mainColor;
        }
      }
      .hint {
        color: #666;
        margin-top: 4px;
        margin-bottom: 4px;
      }
      p {
        line-height: 1.8;
        font-size: 10px;
      }
      .resolve {
        padding-left: 10px;
        &::before{
          content: '-';
          margin-left: -9px;
          margin-right: 3px;
        }
      }
    }
  }
</style>
