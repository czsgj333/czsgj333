<template>
  <div>
    <h1>个人Blog</h1>
    <Pager
      :current="current"
      :total="total"
      @pageChange="handlePageChange($event)"
    />
  </div>
</template>

<script>
import Pager from "./index.vue";
export default {
  components: {
    Pager,
  },
  methods: {
    handlePageChange(newPage) {
      this.current = newPage;
    },
  },
  data() {
    return {
      current: 1,
      total: 302,
    };
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
