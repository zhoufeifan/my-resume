<template>
  <div class="containers">
    <p class="content">
      主攻web前端开发，3年前端开发经验，web基础扎实、熟悉http网络请求。有过移动端网页开发经验，解决过移动端因机型、版本、平台引起的兼容性问题。有过nw与electron客户端的开发经验，踩过许多window客户端的坑。
    </p>
    <p class="content">
      熟悉React、Vue、Jquery等基础框架，熟悉webpack等前端构建工具，对其原理也有一定的了解。掌握git的基本命令，了解Linux脚本常用的一些命令，忠实的mac用户。
    </p>
    <p class="content">
      线下学习过node，参照vue-cli，用node为公司写了一个前端发布脚本。
      使用 node + koa + MongoDB 实现一个todoList 的网站 
      <a href="http://todolist.zhoufeifan.tech/dist/index.html#/">http://todolist.zhoufeifan.tech/dist/index.html</a>。
    </p>
    <p class="content">有过微信端、钉钉端等容器中网站应用开发的经验, 目前疯狂踩坑中</p>
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
