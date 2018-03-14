<template>
  <div class="resume-container">
    <Header></Header>
    <div class="resume-content">
      <ItemTitle title="工作经历" :icon="require('../assets/img/test.svg')">
        <DraftItem>
          <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
        </DraftItem>
        <DraftItem>
          <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
        </DraftItem>
        <DraftItem>
          <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
        </DraftItem>
        <DraftItem>
          <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
        </DraftItem>
        <DraftItem>
          <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
        </DraftItem>
      </ItemTitle>
      <ItemTitle title="项目经理" :icon="require('../assets/img/test.svg')">
      </ItemTitle>
      <ItemTitle title="技能掌握" :icon="require('../assets/img/test.svg')">
      </ItemTitle>
      <ItemTitle title="兴趣爱好" :icon="require('../assets/img/test.svg')">
      </ItemTitle>
      <ItemTitle title="自我评价" :icon="require('../assets/img/test.svg')">
      </ItemTitle>
    </div>
  </div>
</template>

<script>
  import Header from '../components/Header.vue';
  import ItemTitle from '../components/ItemTitle.vue';
  import DraftItem from '../components/DraftItem.vue';
  export default {
      components: {
        Header,
        ItemTitle,
        DraftItem
      }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
.resume-container {
  overflow: hidden;
  background-color: white;
  border-radius: 4px;
  margin: 30px 50px;
  box-shadow: 0 2px 16px 0 rgba(73,73,73,.1);
  .resume-content{
    padding: 30px;
  }
}
</style>
