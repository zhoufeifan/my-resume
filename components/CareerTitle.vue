<template>
  <div class="career-title">
    <div class="time">{{time}}</div>
    <div class="company">{{company}}</div>
    <div class="job">{{job}}</div>
  </div>
</template>

<script>
  export default {
    name: 'CareerTitle',
    props: {
      time: String,
      company: String,
      job: String
    },
  };
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
  .career-title{
    display: flex;
    font-size: 14px;
    .time{
      width: 200px;
    }
    .company,.job{
      flex: 1;
    }
    .job {
      padding-right: 20px;
      text-align: right;
    }
    @include Height(24px);
    margin-bottom: 10px;
  }
</style>
