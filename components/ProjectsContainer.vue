<template>
  <div class="containers">
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">NW.js</span>
      </div>
      <p class="project-name">采宝收银台</p>
      <p class="project-description">冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发</p>
    </div>
    <div class="project-container">
      <div class="skill-tags">
        <span class="tag-item">React</span>
        <span class="tag-item">webpack</span>
      </div>
      <p class="project-name">采宝商家后台</p>
      <p class="project-description">
        冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发
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
        冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发
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
      margin-top: 15px;
      line-height: 20px;
    }
  }
</style>
