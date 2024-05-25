<template>
  <i class="iconfont icon_container" :class="fontClass"></i>
</template>

<script>
const classMap = {
  home: "icon-shouye",
  success: "icon-chenggong",
  error: "icon-error",
  close: "icon-close",
  warn: "icon-warning",
  info: "icon-info",
  blog: "icon-blog",
  code: "icon-code",
  about: "icon-about",
  weixin: "icon-weixin",
  mail: "icon-mail",
  github: "icon-github",
  qq: "icon-qq",
  arrowUp: "icon-arrowup",
  arrowDown: "icon-arrow_down",
  empty: "icon-empty",
  chat: "icon-chat",
};
export const types = Object.keys(classMap);
export default {
  props: {
    type: {
      type: String,
      required: true,
    },
  },
  computed: {
    // 图标类样式
    fontClass() {
      return classMap[this.type];
    },
  },
};
</script>

<style scoped>
@import "//at.alicdn.com/t/c/font_4553163_y7qa30qsghr.css";
</style>
