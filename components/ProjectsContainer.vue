<template>
  <div class="containers">
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">NW.js</span>
      </div>
      <p class="project-name">采宝收银台</p>
      <p class="project-description">
        项目描述：是一个运行在PC客户端的收银软件。收银员通过扫描消费者的付款码，从而完成交易。还有交易报表查询以及商家会员卡券核销的功能。
      </p>
      <p class="project-description">
        涉及技术：使用Nw.js作为客户端支持，是React作为主要框架的单页面应用。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">webpack</span>
      </div>
      <p class="project-name">采宝商家后台</p>
      <p class="project-description">
        项目描述：是一个商户专用的网站平台，商家可以在这个平台上传个人资料信息，来实现与支付宝、微信进行收款签约。也可以在平台上查询自己的交易、会员、消费者等数据。
      </p>
      <p class="project-description">
        涉及技术：项目由React编写，包含了多个单页面应用，且共用一套组件，打包编译速度成了根本的问题。因此用webpack 实现了公共模块的抽离，组件模块的动态加载，从而提升打包的效率。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">Vue</span>
        <span class="tag-item">H5</span>
        <span class="tag-item">支付宝、微信</span>
      </div>
      <p class="project-name">扫码支付页面</p>
      <p class="project-description">
      项目描述：消费者可以通过使用支付宝或者微信扫一扫来进入这个页面，输入金额、选择卡券或者活动，通过支付宝或者微信支付向商家付款。
      </p>
      <p class="project-description">
        涉及技术：主要框架Vue，使用了flex、rem 等响应式布局，css3动画效果。
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ProjectContainer',
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
      font-size: 16px;
      margin-bottom: 15px;
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
      }
    }
    .project-description{
      width: 600px;
      margin-top: 10px;
      line-height: 1.5;
    }
  }
</style>
