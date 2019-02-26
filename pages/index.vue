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
              <CareerTitle time="2018.05 — 至今" company="杭州光云科技有限公司" job="前端开发"></CareerTitle>
              <div class="work-content-list">
                <div class="work-content">
                  <p class="title">
                    快麦收银软件
                    <span class="skill">Electron、Web、Node</span>
                  </p>
                  <p class="hint">项目描述：是一款用于桌面端的收银软件，主要功能有秤重、会员折扣计价、收款、打印小票等，对接了条码秤、电子秤、打印机、读卡器等多个硬件设备。</p>
                  <p class="resolve">针对硬件设备与web通信在不同收银机上的兼容性问题，将通信方式从原来的websocket方式改为Electorn原生的进程通信方式，并采用消息节流的方式提升性能，最终解决了这个问题。</p>
                </div>
                <div class="work-content">
                  <p class="title">
                    番茄表单
                    <span class="skill">Vue全家桶、微信与钉钉应用</span>
                  </p>
                  <p class="hint">项目描述：B端用户在B端创建表单后，生成表单链接，用户通过这个链接打开一个表单，就可以填写相关的信息。主要的应用场景有“问卷调查”、“考试测评”、“投票选举”、“信息收集”等功能。</p>
                  <p class="resolve">针对运营方面定期产出的需求（首页banner、广告弹窗、公告等）。和同事合作一起搭建了一个后台管理系统，让那些需求通过后台系统配置的方式实现，解决了90%来自运营那边的需求。</p>
                  <p class="resolve">编写了一个消息提示框插件，通过全局注入到项目中。用一行代码代替原来分散的多行代码实现消息提示框的功能，提升开发效率、降低代码维护成本。</p>
                  <p class="resolve">针对移动端填表不同设备兼容性问题的排查， 做了报错信息收集上报的功能。通过捕获全局的错误信息，解析堆栈调用，并获取用户的设备型号、网络环境、应用版本等信息进行上报。</p>
                </div>
                <div class="work-content">
                  <p class="title">
                    有成会议移动端报名
                    <span class="skill">Vue全家桶、CSS 3 </span>
                  </p>
                  <p class="hint">项目描述：有成会议移动端报名页面，用户通过手机号进行参会人员的添加、查询、删除等，还可以通过微信支付进行报名缴费。</p>
                  <p class="resolve">针对在微信webview中网页下拉的糟糕体验，设计了一个组件，让页面既可以有效的防止下拉，又可以流畅地进行滚动，实现仿原生的体验。</p>
                </div>
              </div>
            </DraftItem>
          </div>
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2016.04 — 2018.05" company="杭州合言信息科技有限公司" job="前端开发"></CareerTitle>
              <div class="work-content">
                <p>
                  1、主要负责『采宝PC收银台』项目，期间对项目进行的不断的改进和调整，前端方面将<span class="main-color">Jquery重构成React</span>，
                  并把项目迁移到 <span class="main-color">create-react-app</span> 项目上。客户端方面从 C# 重构为<span class="main-color">NW.js</span>，解决了许多客户端兼容的问题，性能、体验以及稳定性都有很大的提升。
                </p>
                <p>
                  2、使用 <span class="main-color">webpack</span> 脚手架管理『采宝商家后台项目』，这是一个集成多个单页面应用的项目，每个页面都会出现一个bundle（包含 <span class="main-color">react、antd</span>），
                  因此打包编译的性能成了关键问题。对此做了许多优化工作（<span class="main-color">模块按需加载、公共模块抽离、happypack</span>等），
                  并尝试了许多方法进行按需打包（文件md5、命令式、读配置文件等）。
                </p>
                <p>3、使用<span class="main-color">Node Js</span> 编写相关的发布脚本，结合 <span class="main-color">git + node + webpack + oss</span>， 使得发布流程规范化与一键化，提高整个前端团队的效率。</p>
                <p>4、在对『采宝会员系统』项目红包雨模块开发中，对<span class="main-color">高并发型</span>红包雨下落动画做了性能优化，在移动端的体验效果从<span class="main-color">卡顿到流畅</span>。</p>
                <p>5、开发过『采宝扫码支付页面』涉及到<span class="main-color">微信网页</span>开发的相关技术，包括用<span class="main-color">户信息授权、api鉴权、微信sdk调用</span>等相关技术。</p>
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
              工作非常注重效率，喜欢合理规划时间。
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
          .work-content-list{
            .work-content{
              margin-right: 10%;
              margin-top: 10px;
              .title {
                font-size: 14px;
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
                  font-size: 12px;
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
