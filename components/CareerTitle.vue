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
    font-size: 16px;
    .time{
      width: 200px;
    }
    .company,.job{
      flex: 1;
    }
    @include Height(24px);
    margin-bottom: 10px;
  }
</style>
