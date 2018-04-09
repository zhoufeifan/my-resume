<template>
  <div class="page-container">
    <a class="download" :href="downloadUrl">下载pdf</a>
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
              <span class="time">2014.12</span>
              <span class="awards">获得《浙江省多媒体设计竞赛》三等奖</span>
            </div>
            <div class="awards-item">
              <span class="time">2014.05</span>
              <span class="awards">获得《浙江省电子商务竞赛》三等奖</span>
            </div>
          </div>
        </ItemTitle>
        <ItemTitle title="工作经历" :icon="require('../assets/img/work.svg')">
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2016.04 — 至今" company="杭州合言信息科技有限公司" job="前端开发（11K）"></CareerTitle>
              <p class="work-content">
                1、负责前端项目的脚手架搭建与配置<br>
                2、负责公司的主流项目『采宝收银台』的开发与维护<br>
                3、参与日常的前端业务开发，包括PC端项目『商家后台』，<br>移动端（支付宝、微信内嵌页面）H5页面的开发<br>
                4、参与前端组件库的开发<br>
                5、参与前端发布脚本的编写
              </p>
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
              不太安分，喜欢研究探索一些新的或者其他领域的技术。
            </p>
            <p class="comment-item">
              有点偏向于完美主义，会对自己之前写的程序做改进优化。
            </p>
            <p class="comment-item">
              对时间有点吝啬，喜欢对事情做四象限分类，会安排自己的todoList
            </p>
          </div>
        </ItemTitle>
      </div>
    </div>
  </div>
</template>

<script>
  import {domain} from '../config.json';
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
      },
      data(){
        return{
          downloadUrl : `${domain}/download/downLoadResumePDF`,
        };
      }
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .page-container{
    width: 800px;
    @include center-block;
    .download{
      font-size: 14px;
      color: #bbbbbb;
      position: absolute;
      top: 8px;
    }
    .resume-container {
      margin-top: 30px;
      margin-bottom: 10px;
      overflow: hidden;
      background-color: white;
      border-radius: 4px;
      box-shadow: 0 2px 16px 0 rgba(73,73,73,.1);
      .resume-content{
        padding: 30px;
        font-size: 14px;
        .school-career-container{
          /*display: flex;*/
          position: relative;
          /*flex-wrap: wrap;*/
          @include clear-fix;
          .awards-item{
            float: left;
            width: 50%;
            /*flex-wrap: wrap;*/
            @include Height(30px);
            &>span{
              display: inline-block;
            }
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
          .work-content{
            width: 514px;
            line-height:2;
          }
        }
        .comment-myself{
          .comment-item{
            position: relative;
            margin-top: 12px;
            padding-left: 16px;
            &::before{
              content: '';
              display: block;
              width: 6px;
              height: 6px;
              border-radius: 50%;
              background-color: black;
              position: absolute;
              left: 0;
              top: 4px;
            }
          }
        }
      }
    }
  }

</style>
