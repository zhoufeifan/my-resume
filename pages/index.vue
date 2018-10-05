<template>
  <div class="page-container">
    <!--<a class="download" :href="downloadUrl">下载pdf</a>-->
    <div class="resume-container">
      <Header></Header>
      <div class="resume-content">
        <ItemTitle title="技能掌握" :icon="require('../assets/img/skill.svg')">
          <!--技能掌握-->
          <SkillManages></SkillManages>
        </ItemTitle>
        <ItemTitle title="工作经历" :icon="require('../assets/img/work.svg')">
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2018.05 — 至今" company="杭州光云科技公司" job="前端开发"></CareerTitle>
              <p class="work-content">
                参与过快麦收银软件的开发，包括web端的与electron端，硬件设备的接入。<br>
                番茄表单网站的优化与改进。<br>
                有成年会C端报名页的开发，用户体验的改进。<br>
                红包雨项目，处理高并发型引起的性能问题。<br>
              </p>
            </DraftItem>
          </div>
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2016.04 — 2018.05" company="杭州合言信息科技有限公司" job="前端开发"></CareerTitle>
              <div class="work-content">
                <p>
                  16年进入公司接触公司的主要产品『采宝收银台』，之后对项目进行的不断的改进和调整，
                  前端方面将jquery重构成React，项目用webpack进行打包构建。客户端方面从C#升级为NW，过程中踩了很多坑，
                  但性能、体验以及稳定性都有很大的提升，间接推动用户量增长。
                </p>
                <p>主要负责部分前端项目的脚手架搭建与配置。带过实习生进行日常的业务开发。</p>
              </div>
            </DraftItem>
          </div>
        </ItemTitle>
        <!-- <ItemTitle title="主要项目经历" :icon="require('../assets/img/project.svg')">
          <ProjectsContainer></ProjectsContainer>
        </ItemTitle> -->
        <ItemTitle title="在校荣誉" :icon="require('../assets/img/school.svg')">
          <div class="school-career-container">
            <div class="awards-item">
              <span class="awards">『浙江省程序设计竞赛』铜奖</span>
            </div>
            <div class="awards-item">
              <span class="awards">浙江海洋大学『王成海』奖学金</span>
            </div>
            <div class="awards-item">
              <span class="awards">『浙江省服务外包竞赛』二等奖</span>
            </div>
            <div class="awards-item">
              <span class="awards">『新苗人才计划项目』项目负责人</span>
            </div>
            <div class="awards-item">
              <span>『浙江省多媒体设计竞赛』三等奖</span>
            </div>
            <div class="awards-item">
              <span class="awards">『浙江省电子商务竞赛』三等奖</span>
            </div>
          </div>
        </ItemTitle>
        <ItemTitle title="自我评价" :icon="require('../assets/img/comment.svg')">
          <!--自我评价-->
          <div class="comment-myself">
            <p class="comment-item">
              不太喜欢安于现状，喜欢研究探索新的技术。
            </p>
            <p class="comment-item">
              有点偏向于完美主义，会对自己之前写的程序做改进优化。
            </p>
            <p class="comment-item">
              喜欢在合适的时间做合适的事情。
            </p>
            <p class="comment-item">
              平时注重锻炼身体，认为身体才是革命的本钱。
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
          font-size: 12px;
          /*display: flex;*/
          position: relative;
          /*flex-wrap: wrap;*/
          @include clear-fix;
          .awards-item{
            float: left;
            font-size: 10px;
            /*margin-right: 20px;*/
            width: 40%;
            /*flex-wrap: wrap;*/
            @include Height(20px);
            @include clear-fix;
            &>span{
              float: left;
              display: block;
            }
          }
          .time{
            width: 60px;
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
            // width: 514px;
            margin-right: 10%;
            line-height:2;
            font-size: 10px;
            p{
              line-height: 1.8;
              margin-top: 10px;
            }
          }
        }
        .comment-myself{
          .comment-item{
            position: relative;
            margin-top: 12px;
            padding-left: 16px;
            font-size: 12px;
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

    .page-container{
        width: 100%;
      .resume-container {
        margin: 0;
        border-radius: 0;
      }
    }

  @media screen and (max-width: 1024px){
    .page-container{
        width: 100%;
      .resume-container {
        margin: 0;
        border-radius: 0;
      }
    }
  }

</style>
