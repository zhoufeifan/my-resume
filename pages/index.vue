<template>
  <div class="resume-container">
    <Header></Header>
    <div class="resume-content">
    </div>
  </div>
</template>

<script>
    import Header from '../components/Header.vue';
    export default {
        components: {
            Header
        }
    }
</script>

<style lang="scss" scoped>
  @import "~assets/mixin.scss";
.resume-container {
  overflow: hidden;
  background-color: white;
  border-radius: 4px;
  margin: 30px 50px;
}
</style>
