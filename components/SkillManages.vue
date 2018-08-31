<template>
  <div class="containers">
    <div class="skill-master-container">
      <p class="skill-name">Web基础</p>
      <p class="skill-description">熟悉JS的语法和知识，并且熟练掌握es5及以上语法</p>
      <p class="skill-description">熟练掌握CSS 规则以及语法，熟练使用SCSS。</p>
      <p class="skill-description">熟练掌握移动web端开发的响应式设计，以及兼容问题的处理。</p>
      <p class="skill-description">熟练掌握Dom的编程操作、Ajax 异步的请求处理。</p>
      <p class="skill-description">熟悉chrome浏览器开发者工具的使用和调试。</p>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">前端框架</p>
      <div class="skill-description">熟练使用React + mobx + react-router 开发大型应用</div>
      <div class="skill-description">熟练使用Vue + vuex + vue-router 开发大型应用</div>
      <div class="skill-description">使用React、Vue + es6 + babel 进行第三方组件的开发</div>
      <div class="skill-description">熟悉 ant-design 、 Jquery 、 BootStrap等其他的流行框架</div>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">Webpack</p>
      <div class="skill-description">熟悉create-react-app 和 vue-cli 的使用，修改基础配置满足个性化需求</div>
      <div class="skill-description">熟悉webpack 中的各种字段的配置</div>
      <div class="skill-description">公共模块抽离、资源的懒加载</div>
      <div class="skill-description">熟练使用 各种 plugins 和 loader</div>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">网络请求</p>
      <div class="skill-description">属性Http协议，对新版的Http2也有了解</div>
      <div class="skill-description">可以通过chrome 调试工具查看网络请求的情况</div>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">服务端</p>
      <div class="skill-description">掌握Nodejs 中常用的api</div>
      <div class="skill-description">运用Nodejs 编写发布脚本</div>
      <div class="skill-description">
        koa + MongoDB 实现一个todoList 的网站
        <br>线上地址:
        <a href="http://todolist.zhoufeifan.tech/dist/index.html#/">
          http://todolist.zhoufeifan.tech/dist/index.html
        </a>
      </div>
      <div class="skill-description">使用 Nuxt.js 搭建了一个人简历的同构应用项目
        <br>
        线上地址:<a href="http://resume.zhoufeifan.tech/">resume.zhoufeifan.tech</a>
      </div>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">客户端应用</p>
      <div class="skill-description">有过nw.js 和 electron 的开发经验，对微信小程序和钉钉E应用也有一定的了解</div>
    </div>
    <div class="skill-master-container">
      <p class="skill-name">其他</p>
      <div class="skill-description">掌握git的基本命令 </div>
      <div class="skill-description">了解Linux脚本常用的一些命令</div>
      <div class="skill-description">Mac、JetBrains 的资深用户</div>
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
      .skill-name{
        font-size: 16px;
        font-weight: bold;
      }
      .skill-description{
        padding-left: 20px;
        position: relative;
        margin-top: 12px;
        line-height: 16px;
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
          top: 5px;
        }
      }
    }
  }
</style>
