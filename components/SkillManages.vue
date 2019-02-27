<template>
  <div class="containers">
    <p class="content">
      1、熟悉前端相关的技术（包括HTML/CSS/JavaScript等），熟悉 ES6 及以上语法。
    </p>
    <p class="content">
      2、具备跨终端（Mobile + PC）的前端开发能力与桌面（Electron、NW）应用开发的实践经验。  
    </p>
    <p class="content">
      3、熟练掌握 使用MVVM（Vue、React）框架开发的技巧，并了解其实现的原理，具备开发大型应用的实践。
    </p>
    <p class="content">
      4、熟悉设计模式相关的知识，可以编写简洁易维护的代码。熟悉性能优化方面的知识，有过移动端的动画效果优化的实践，<a href="http://blog.zhoufeifan.tech/demo/dist/index.html#/redpacket">点击查看 demo</a>。
    </p>
    <p class="content">
      5、熟悉网络协议（HTTP/SSL）以及常见安全问题和对策，具备前端工程化与模块化开发的实践经验。
    </p>
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
    .content{
      line-height: 1.5;
      margin-right: 10%;
      font-size: 12px;
      &+.content{
        margin-top: 10px;
      }
    }
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
