<template>
  <div id="app" ref="app" class="theme-red">
    <HeaderWrap></HeaderWrap>
    <router-view/>
  </div>
</template>

<script>
import HeaderWrap from 'components/header/header.vue'
import { mapGetters } from 'vuex'
export default {
  name: 'app',  
  components:{
    HeaderWrap
  }
}
</script>

<style>

</style>
