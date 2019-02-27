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
                    番茄表单
                    <span class="skill">Vue全家桶、微信与钉钉应用</span>
                  </p>
                  <p class="hint">项目描述：B端用户在B端创建表单后，生成表单链接，用户通过这个链接打开一个表单，就可以填写相关的信息。主要的应用场景有“问卷调查”、“考试测评”、“投票选举”、“信息收集”等功能。</p>
                  <p class="resolve">针对运营方面定期产出的需求（首页banner、广告弹窗、公告等）。和同事一起搭建了一个后台管理系统，让那些需求通过后台系统配置的方式实现，解决了90%来自运营那边的需求。</p>
                  <p class="resolve">编写了一个消息提示框插件，通过全局注入到项目中。用一行代码代替原来分散的多行代码实现消息提示框的功能，提升开发效率、降低代码维护成本。</p>
                  <p class="resolve">针对移动端填表不同设备兼容性问题的排查， 做了报错信息收集上报的功能。通过捕获全局的错误信息解析堆栈调用，并获取用户的设备型号、网络环境、应用版本等信息进行上报。最终通过对应的机型上调试，解决了相关的问题。</p>
                </div>
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
              <WorkExperience :workList="caibaoWorkList"/>
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
              对新的技术充满好奇与兴趣。
            </p>
            <p class="comment-item">
              一旦发现更好的解决方案，会花时间去改进原来的代码。
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
  import WorkExperience from '../components/WorkExperience.vue';
  import ProjectsContainer from '../components/ProjectsContainer.vue';
  import SkillManages from '../components/SkillManages.vue';

  export default {
      components: {
        Header,
        ItemTitle,
        DraftItem,
        CareerTitle,
        ProjectsContainer,
        WorkExperience,
        SkillManages
      },
      data(){
        return{
          downloadUrl : `${domain}/download/downLoadResumePDF`,
          caibaoWorkList: [{
            title: '采宝收银台',
            skill: 'NW.js、React、Node',
            desc: '是一款运行在 window 桌面端的收银软件，主要功能有扫码收款、现金记账、订单明细查询、报表生成等。',
            resolves:[
              '旧版本的软件是用C#环境集成客户端，存在许多兼容性的问题，要写很多兼容代码，影响开发效率。结合实际业务的场景以及和同事之间的讨论结果，最终选定了NW.js代替C#，解决了95%的兼容问题，并且性能和稳定性都有所提升。',
              '对项目的Web端也做了重构，将原来的Jquery 重构成 React,并用 webpack 管理项目，实现项目的模块化与工程化。'
            ]
          }, {
            title: '采宝商家中心',
            skill: 'webpack、antd、React',
            desc: '是一个面向商家的管理平台，商家可以在平台上管理自己的门店、活动、会员，可以按年、月、日查看自己的交易明细等。',
            resolves:[
              `这是一个集成多个单页面应用的项目，每个页面都会出现一个bundle（包含react、antd），因此打包编译的速度成了关注的焦点。针对该问题主要从两方面入手。一方面改造webpack脚手架，采用模块按需加载、公共模块抽离、happypack等套路提升打包速度。
              另一方面引入按需打包的方法，由开发人员指定这次发布要打包的页面，很大程度上提升了编译打包的速度。`,
            ]
          },{
            title: '采宝会员系统',
            skill: 'Vue全家桶、微信应用',
            desc: '是一款对接商家微信公众号的会员系统，主要功能包括微信授权注册会员、优惠券的领取与核销、会员充值等功能',
            resolves: [
              '为了解决H5端原生键盘体验差的问题，自己用js写了一个数字键盘组件，添加了点击效、弹出、收起的动画效果，达到了良好的体验效果。',
              `在做红包雨游戏模块时，一开始使用anime.js实现红包下落翻转的动画效果，但是一旦这个动画的并发次数变多时，页面就会出现卡顿的问题。针对这个问题，使用纯CSS 效果代替js实现动画效果，
              并采用dom批量预创建的方式减少dom创建的次数。最终解决了高并发下动画卡顿的问题，<a href="http://blog.zhoufeifan.tech/demo/dist/index.html#/redpacket">点击查看效果demo</a>`,
            ]
          }]
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
