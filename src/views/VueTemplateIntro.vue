<template>
  <div class="App">
    <!-- header -->
    <Header :title="title" :show="isShow"></Header>

    <!-- page -->
    <div class="page">
      <ul class="advantage">
        <li>基于Vue-cli3.0进行制作。</li>
        <li>遵循Wlk-cli集成规范。</li>
        <li>允许开发者自由定制。</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Header from '../components/Header/Header';
import { mapState, mapActions } from 'vuex';
import '../common/css/index.less';
export default {
  name: '',
  components: {
    Header: Header
  },
  data() {
    return {
      title: 'Vue 模板说明',
      isShow: true
    };
  }
};
</script>
<style lang="less" scoped>
.App {
  padding: 0px;

  .page {
    .advantage {
      text-align: left;

      li {
        padding-left: 15px;
        border-bottom: 1px solid #eee;
        line-height: 3em;
        font-size: 14px;
      }
    }
  }
}
</style>
