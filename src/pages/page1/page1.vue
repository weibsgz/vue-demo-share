<template>
    <div class="sass-wrap">
      <div class="test-sass">
        sass测试容器 sass测试容器 sass测试容器 sass测试容器
      </div>
    </div>

</template>

<script type="text/javascript">

  export default {
     name: 'page1'
  }
</script>

<style lang="scss" scoped>
  @import "~assets/css/lib-variable";
  @import "~assets/css/lib-mixin";
  /*SASS的常用变量 宏 已定义在assets/css/variable  mixin里*/
  .sass-wrap {
    position:relative;
    height:calc(100vh - 40px);
    .test-sass{
      color:$cl-txt;
      @include center(200px,200px);
      @include linear($color1: #000, $color2: #fff, $angle: 180deg);     
      @include no-wrap;

    }
  }

</style>
