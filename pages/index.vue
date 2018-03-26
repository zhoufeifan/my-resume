<template>
  <div class="resume-container">
    <Header></Header>
    <div class="resume-content">
      <ItemTitle title="在校经历" :icon="require('../assets/img/school.svg')">
        <div class="school-career-container">
          <div class="awards-item">
            <span class="time">2015.12</span>
            <span class="awards">获得浙江海洋大学『王成海』奖学金</span>
          </div>
          <div class="awards-item">
            <span class="time">2015.05</span>
            <span class="awards">获得《浙江省服务外包竞赛》二等奖</span>
          </div>
          <div class="awards-item">
            <span class="time">2015.04</span>
            <span class="awards">获得《浙江省程序设计竞赛》铜奖</span>
          </div>
          <div class="awards-item">
            <span class="time">2013.11-2015.3</span>
            <span class="awards">负责《新苗人才计划项目》成功结业</span>
          </div>
          <div class="awards-item">
            <span class="time">2014.05</span>
            <span class="awards">获得《浙江省电子商务竞赛》三等奖</span>
          </div>
          <div class="awards-item">
            <span class="time">2014.12</span>
            <span class="awards">获得《浙江省多媒体设计竞赛》三等奖</span>
          </div>
        </div>
      </ItemTitle>
      <ItemTitle title="工作经历" :icon="require('../assets/img/work.svg')">
        <div class="draft-group">
          <DraftItem>
            <CareerTitle time="2016.04 — 至今" company="杭州合言信息科技有限公司" job="前端开发"></CareerTitle>
            <p>冯萨芬就冯撒酒疯就会i就冯萨芬范德萨发撒冯萨芬冯萨芬撒</p>
          </DraftItem>
        </div>
      </ItemTitle>
      <ItemTitle title="主要项目经历" :icon="require('../assets/img/project.svg')">
        <!--项目经历-->
        <ProjectsContainer></ProjectsContainer>
      </ItemTitle>
      <ItemTitle title="技能掌握" :icon="require('../assets/img/skill.svg')">
        <!--技能掌握-->
        <SkillManages></SkillManages>
      </ItemTitle>
      <ItemTitle title="自我评价" :icon="require('../assets/img/comment.svg')">
        <!--自我评价-->
        <div class="comment-myself">
          <p class="comment-item">
            1、冯萨芬拉萨就发了撒街坊邻居风流三国
          </p>
          <p class="comment-item">
            1、冯萨芬拉萨就发了撒街坊邻居风流三国
          </p>
          <p class="comment-item">
            1、冯萨芬拉萨就发了撒街坊邻居风流三国
          </p>
        </div>
      </ItemTitle>
    </div>
  </div>
</template>

<script>
  import Header from '../components/Header.vue';
  import ItemTitle from '../components/ItemTitle.vue';
  import DraftItem from '../components/DraftItem.vue';
  import CareerTitle from '../components/CareerTitle.vue';
  import ProjectsContainer from '../components/ProjectsContainer.vue';
  import SkillManages from '../components/SkillManages.vue';

  export default {
      components: {
        Header,
        ItemTitle,
        DraftItem,
        CareerTitle,
        ProjectsContainer,
        SkillManages
      }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
.resume-container {
  overflow: hidden;
  background-color: white;
  border-radius: 4px;
  margin-top: 30px;
  @include center-block;
  width: 800px;
  /*margin: 30px 50px;*/
  box-shadow: 0 2px 16px 0 rgba(73,73,73,.1);
  .resume-content{
    padding: 30px;
    font-size: 14px;
    .school-career-container{
      display: flex;
      position: relative;
      flex-wrap: wrap;
      .awards-item{
        width: 50%;
        flex-wrap: wrap;
        /*flex: 1;*/
        @include Height(30px);
        &>span{
          display: inline-block;
        }
        /*&:first-child{*/
          /*font-weight: bold;*/
          /*font-size: 14px;*/
          /*margin-bottom: 8px;*/
        /*}*/
      }
      .time{
        width: 108px;
      }
    }
    .draft-group{
      position: relative;
      z-index: 1;
      &::after{
        position: absolute;
        content: " ";
        width: 1px;
        height: 100%;
        top: 0;
        left: 0;
        opacity: .5;
        background-color: $mainColor;
      }
    }
    .comment-myself{
      .comment-item{
        margin-top: 10px;
      }
    }
  }
}
</style>
