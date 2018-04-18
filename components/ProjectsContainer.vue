<template>
  <div class="containers">
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">NW.js</span>
      </div>
      <p class="project-name">采宝收银台</p>
      <p class="project-description">
        项目描述：是一个运行在PC客户端的收银软件。主要的功能有：扫码收款、商品收银、会员的注册与充值、交易报表的查询、以及订单小票的打印。
      </p>
      <p class="project-description">
        涉及技术：使用Nw.js作为客户端支持，是集成React + React-Router + Mobx 的单页面应用程序。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">webpack</span>
      </div>
      <p class="project-name">采宝商家后台</p>
      <p class="project-description">
        项目描述：是一个商户专用的大型网站平台，涉及的功能点很多，具体可以抽象为表单数据的提交、筛选条件进行数据查询、图表的绘制。
      </p>
      <p class="project-description">
        涉及技术：Webpack 配置多个单页面应用、公共模块的抽离、组件的动态加载。用node 实现文件的懒编译， 用 React + ant-design 进行组件化开发。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">Vue</span>
        <span class="tag-item">H5</span>
        <span class="tag-item">支付宝、微信</span>
      </div>
      <p class="project-name">商家会员系统</p>
      <p class="project-description">
      项目描述：运行在支付宝或者微信H5页面的会员系统，主要的功能点会员的注册、充值、详情的展示、卡券的领取、商家活动的展示。
      </p>
      <p class="project-description">
        涉及技术：主要框架Vue全家桶，使用了flex、rem 等响应式布局，css3动画效果，路由的懒加载。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">Vue</span>
        <span class="tag-item">H5</span>
        <span class="tag-item">支付宝、微信</span>
      </div>
      <p class="project-name">商家二维码支付系统</p>
      <p class="project-description">
      项目描述：运行在支付宝或者微信H5页面的支付系统，消费者通过支付宝或者微信扫描商家的二维码进入系统，输入金额，向进行商家付款。
      </p>
      <p class="project-description">
        涉及技术：主要框架Vue全家桶，使用了flex、rem 等响应式布局，css3动画效果。
      </p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">node</span>
        <span class="tag-item">shell</span>
        <span class="tag-item">git</span>
      </div>
      <p class="project-name">前端发布脚本</p>
      <p class="project-description">
      项目描述：参考vue-cli 开发的前端资源发布的命令行工具。
      主要的功能：集中打包项目的资源到测试环境、预发环境、以及线上环境，
      并自动进行相应的git的操作，实现一键化发布流程。
      </p>
      <p class="project-description">
        涉及技术：node.js、ali-oss、shell、puppeteer等。
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
      font-size: 14px;
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
        font-size: 12px;
      }
    }
    .project-description{
      /*width: 600px;*/
      font-size: 12px;
      width: 80%;
      margin-top: 10px;
      line-height: 1.5;
    }
  }
</style>
