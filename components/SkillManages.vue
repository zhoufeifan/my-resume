<template>
  <div class="containers">
    <div class="skill-master-container">
      <p class="skill-name">哈哈哈哈</p>
      <p class="skill-description">冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发</p>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">哈哈哈哈</p>
      <div class="skill-description">
        冯萨芬撒发神经啊发链接撒练腹肌发撒发烧冯萨芬撒发<br>佛挡杀佛2烦死啦放假了
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'SkillManages',
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .containers{
    .skill-master-container{
      &:not(:last-child){
        margin-bottom: 30px;
      }
      .skill-description{
        margin-top: 15px;
        line-height: 20px;
      }
    }
  }
</style>
