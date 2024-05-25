<template>
  <div>
    <h1>个人Blog</h1>
    <div class="test-container">
      <div class="item" v-for="t in types" :key="t">
        <Icon :type="t" />
        <label>{{ t }}</label>
      </div>
    </div>
  </div>
</template>

<script>
import Avatar from "./components/Avatar";
import Pager from "./components/Pager";
import Icon, { types } from "./components/Icon";
export default {
  name: "App",
  components: {
    Avatar,
    Pager,
    Icon,
  },
};
</script>
<style scoped>
/* 加上scoped可以影响子元素的根元素的样式，最多 */
.iconfont {
  color: red;
  font-size: 26px;
}
</style>
