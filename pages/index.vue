<template>
  <div class="page-container">
    <!--<a class="download" :href="downloadUrl">下载pdf</a>-->
    <div class="resume-container">
      <Header></Header>
      <div class="resume-content">
        <!-- <ItemTitle title="主要项目" :icon="require('../assets/img/project.svg')">
          <ProjectsContainer :itemList="projectList" />
        </ItemTitle>
        <div class="blank"></div> -->
        <ItemTitle title="技能掌握" :icon="require('../assets/img/skill.svg')">
          <!--技能掌握-->
          <SkillManages></SkillManages>
        </ItemTitle>
        <ItemTitle title="工作经历" :icon="require('../assets/img/work.svg')">
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2019.05 — 至今" company="杭州大搜车汽车服务有限公司" job="部门前端leader"></CareerTitle>
              <!-- <WorkExperience :workList="raycloundWorkList"/> -->
              <p class="title">主要职责：</p>
              <p class="item-row">1、带领前端团队成功交付 “沃世界” 项目，主要负责小程序与PC管理后台的技术选型、项目login框架与request框架的设计，把控团队的开发节奏解并帮助团队成员解决技术上的卡点，保证项目进度的可控性。</p>
              <p class="item-row">2、负责“CMS系统的开发”，页面组件颗粒度化，实现C端页面的个性化自由搭建，“0开发投入”满足运营人员完成各种活动和文章页面的需求。</p>
            </DraftItem>
          </div>
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2018.05 — 2019.05" company="杭州光云科技有限公司" job="高级前端开发"></CareerTitle>
              <!-- <WorkExperience :workList="raycloundWorkList"/> -->
              <p class="title">主要职责：</p>
              <p class="item-row">1、负责 “番茄表单” C端应用的开发，实现了一套跨平台的 js-sdk 来应对不同平台的 API 差异</p>
              <p class="item-row">2、负责C端应用异常监控系统的开发，可以收集相关的报错信息并及时地进行通知，方便研发快速响应并准确的定位问题。</p>
            </DraftItem>
          </div>
          <div class="draft-group">
            <DraftItem>
              <CareerTitle time="2016.04 — 2018.05" company="杭州合言信息科技有限公司" job="前端开发"></CareerTitle>
              <!-- <WorkExperience :workList="caibaoWorkList"/> -->
              <p class="title">主要职责：</p>
              <p class="item-row">1、负责 “采宝收银台” 桌面应用软件的开发，根据遗留的问题与实际的业务场景，升级技术框架，使用 NW.js 代替 C#，提升了收银软件的稳定性与兼容性，间接推动商户的拓展。</p>
              <p class="item-row">2、开发了一套命令行工具用于前端代码的发布，代替了原来繁琐且机械化的操作流程，一定程度上提升了效率</p>
            </DraftItem>
          </div>
        </ItemTitle>
        <!-- <ItemTitle title="在校荣誉" :icon="require('../assets/img/school.svg')">
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
        </ItemTitle> -->
        <ItemTitle title="自我评价" :icon="require('../assets/img/comment.svg')">
          <!--自我评价-->
          <div class="comment-myself">
            <p class="comment-item">
              习惯每周对工作做总结、反思，遗留的问题会加入自己的 todolist
            </p>
            <p class="comment-item">
              始终坚持 “to be better” 的原则，一旦更好的解决方案，就会去做改进。
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
        return {
          downloadUrl : `${domain}/download/downLoadResumePDF`,
          projectList: [{
            name: '搜车库项目',
            skills: ['Vue','移动端适配'],
            resolve: '自定义实现酷炫的视频播放器，具备流畅的动画效果与操作体验。并且解决了视频截帧图随进度条的拖而动而频繁切换的卡顿问题。'
          },{
            name: 'CMS设计框架',
            skills: ['Drag API','React'],
            resolve: '实现通过拖拽控件的方式来完成页面的搭建，支持页面中拖拽控件。对其展示顺序进行排版。还能支持非顺序性的控件显示（吸底的按钮）。'
          },{
            name: '采宝收银台',
            skills: ['NW.js', 'React', 'Node'],
            resolve: '为解决js在不同浏览器上的兼容性的问题，升级了原来的客户端框架，从 C# 到 NW.js，前端项目通过 webpack 进行工程化提升开发效率。前端资源采用离线缓存，借助 NW.js 的 node 环境，实现资源的在线更新。'
          }],
          raycloundWorkList: [{
            title: '番茄表单',
            skill: 'Vue 全家桶、微信与钉钉应用',
            // desc: 'B端用户在B端创建表单后，生成表单链接，用户通过这个链接打开一个表单，就可以填写相关的信息。主要的应用场景有“问卷调查”、“考试测评”、“投票选举”、“信息收集”等功能。',
            resolves: [
              // '针对运营方面定期产出的需求（首页 banner 、广告弹窗、公告等），和同事一起搭建了一个后台管理系统，让那些需求通过后台系统配置的方式实现，解决了 90% 来自运营那边的需求。',
              '针对解析大文件长时间阻塞的问题，采用了 Web Worker 开启多线程的方案，使得解析任务异步运行，保证页面流畅。',
              '基于对重复代码的零容忍。使用注入插件以及mixin等方式，集成公共的方法与属性，例如：消息弹框、用户信息、http 请求等，提高代码的复用性。',
              // '针对移动端填表不同设备兼容性问题的排查， 做了报错信息收集上报的功能。通过捕获全局的错误信息解析堆栈调用，并获取用户的设备型号、网络环境、应用版本等信息进行上报。最终通过对应的机型上调试，解决了相关的问题。'
            ]
          }, {
            title: '快麦收银软件',
            skill: 'Electron、Web、Node',
            // desc: '是一款用于桌面端的收银软件，主要功能有秤重、会员折扣计价、收款、打印小票等，对接了条码秤、电子秤、打印机、读卡器等多个硬件设备。',
            resolves: ['针对硬件设备与web通信在不同收银机上的兼容性问题，将通信方式从原来的websocket方式改为Electorn原生的进程通信方式，并采用消息节流的方式提升性能，最终解决了这个问题。']
          }, {
            title: '有成会议移动端报名',
            skill: 'Vue 全家桶、CSS3',
            // desc: '有成会议移动端报名页面，用户通过手机号进行参会人员的添加、查询、删除等，还可以通过微信支付进行报名缴费。',
            resolves: ['为了解决在微信 webview 中网页下拉的糟糕体验，设计了一个组件，让页面既可以有效的防止下拉，又可以流畅地进行滚动，实现仿原生的体验。']
          }],
          caibaoWorkList: [{
            title: '采宝收银台',
            skill: 'NW.js、React、Node',
            // desc: '是一款运行在 window 桌面端的收银软件，主要功能有扫码收款、现金记账、订单明细查询、报表生成等。',
            resolves:[
              '旧版本的软件是用C#环境集成客户端，存在许多兼容性的问题。结合实际业务的场景最终选定了 NW.js 代替 C#，解决了95%的兼容问题，并且性能和稳定性都有所提升。',
              '对项目的Web端也做了重构，将原来的 Jquery 重构成 React,并用 webpack 管理项目，实现项目的模块化与工程化。'
            ]
          }, {
            title: '采宝商家中心',
            skill: 'webpack、antd、React',
            // desc: '是一个面向商家的管理平台，商家可以在平台上管理自己的门店、活动、会员，可以按年、月、日查看自己的交易明细等。',
            resolves:[
              `这是一个集成多个单页面应用的项目，每个页面都会出现一个bundle（包含react、antd），因此打包编译的速度成了关注的焦点。针对该问题主要从两方面入手。一方面改造webpack脚手架，采用模块按需加载、公共模块抽离、happypack等套路提升打包速度。
              另一方面引入按需打包的方法，由开发人员指定这次发布要打包的页面，很大程度上提升了编译打包的速度。`,
            ]
          },{
            title: '采宝发布工具',
            skill: 'node、git、oss',
            // desc: '是一款由运行在 node 环境的命令行工具，集成了一键化发布、分支管理、tag 标记等命令。',
            resolves:[
              `针对每个项目发布流程机械化的问题，和同事一起编写了一套基于 node 的命令行工具。只需要一个命令就能让脚本自动去执行发布流程，避免因人为失误而造成的发布问题，提高发布效率。`,
            ]
          },{
            title: '采宝会员系统',
            skill: 'Vue 全家桶、微信应用',
            // desc: '是一款对接商家微信公众号的会员系统，主要功能包括微信授权注册会员、优惠券的领取与核销、会员充值等功能',
            resolves: [
              '为了解决 H5 端原生键盘体验差的问题，自己用 js 写了一个数字键盘组件，添加了点击效、弹出、收起的动画效果，达到了良好的体验效果。',
              `在做红包雨游戏模块中使用纯 CSS 效果代替 JS 实现动画效果，并采用 dom 批量预创建的方式减少 dom 创建的次数。最终解决了高并发下动画卡顿的问题，<a href="http://blog.zhoufeifan.tech/demo/dist/index.html#/redpacket">点击查看效果 demo</a>`,
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
          .title {

          }
          .item-row {
            font-size: 12px;
            line-height: 1.3;
            margin-top: 10px;
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
  .blank {
    height: 70px;
  }
</style>
