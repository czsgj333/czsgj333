<template>
  <div class="pager_container">
    <a href="" :class="{disabled: current === 1}">|&lt;&lt;</a>
    <a href="" :class="{disabled: current === 1}">&lt;&lt;</a>
    <!-- a*10>{$} 快速生成10个随意数字 -->
    <a href="">1</a>
    <a href="" class="actived">2</a>
    <a href="">3</a>
    <a href="">4</a>
    <a href="">5</a>
    <a href="">6</a>
    <a href="">7</a>
    <a href="">8</a>
    <a href="">9</a>
    <a href="" :class="{disabled: current === pageNumber}">&gt;&gt;</a>
    <a href="" :class="{disabled: current === pageNumber}">&gt;&gt;|</a>
  </div>
</template>

<style  lang="less" scoped> 
@import "~@/styles/var.less";
    .pager_container {
        display: flex;
        margin: 20px 0;
        justify-content: center;
        a{
            color: @primary;
            margin: 0 6px; 
            &.disabled{
                color: @lightWords;
                cursor: not-allowed;
            }
            &.actived{
                color: @words;
                font-weight: bold;
                cursor: text;
            }
        }
    }
</style>
<script>
export default {
    props:{
        current:{
            type: Number,
            default: 1
        },
        total:{
            type: Number,
            default: 0
        },
        limit:{
            type: Number,
            default: 10
        },
        visibleNumber:{
            type: Number,
            default: 10
        }
    },
    computed:{
        // 总页数
        pageNumber(){
           return Math.ceil(this.total / this.limit)
        }
    }
}
</script>

