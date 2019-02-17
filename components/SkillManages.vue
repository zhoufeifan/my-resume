<template>
  <div class="containers">
    <p class="content">
      1、熟练掌握JS基础、ES6及以上语法。熟悉 HTML 与 CSS 以及浏览器相关的知识。  
    </p>
    <p class="content">
      2、主要技术栈为 Vue，熟练掌握其开发技巧，了解其实现的原理。React 方面也有相关的项目经验。
    </p>
    <p class="content">
      3、了解设计模式相关的知识，可以编写简洁易维护的代码。
    </p>
    <p class="content">
      4、了解性能优化方面的知识，优化过 H5 动画效果, 从卡顿到流畅。
    </p>
    <p class="content">
      5、熟悉 http、https 相关的知识
    </p>
    <p class="content">
      6、熟悉Wepack的使用，熟悉其配置各种项以及loader、plugin的使用，编写过自定义的 loader 与 plugin。
    </p>
    <p class="content">
      7、具备客户端应用开发的经验，包括 electron、nw 以及移动端 webapp, 解决过许多兼容性问题。 
    </p>
    <p class="content">
      8、自主学习了 NodeJS， 编写了一个自动化发布发布脚本，为整个团队提升了 5% 的研发效率。
      并且学习了 koa、 MongoDB 以及服务器部署的相关知识，搭建了一个 <a href="http://todolist.zhoufeifan.tech/dist/index.html#/">todoList</a> 的网站。 
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
