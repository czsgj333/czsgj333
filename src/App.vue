<template>
  <div>
    <h1>个人Blog</h1>
    <Avatar url="http://gips3.baidu.com/it/u=3886271102,3123389489&fm=3028&app=3028&f=JPEG&fmt=auto?w=1280&h=960" :size="150"></Avatar>
    <Avatar url="https://c-ssl.duitang.com/uploads/item/201610/08/20161008230120_QfAYw.jpeg"></Avatar>
    <Pager type="home"></Pager>
  </div>
</template>

<script>
import Avatar from "./components/Avatar.vue";
import Pager from "./components/Pager.vue"
export default{
  name: "App",
  components:{
    Avatar,
    Pager
  }
}
</script>
<style scoped>
 /* 加上scoped可以影响子元素的根元素的样式，最多 */
 .iconfont{
  color: red;
  font-size: 26px;
 }
</style>