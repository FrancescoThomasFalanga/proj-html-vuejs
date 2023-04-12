<script>
import AppHeader from './components/AppHeader.vue';
import AppPro from './components/AppPro.vue';
import AppServices from './components/AppServices.vue';
import AppShop from './components/AppShop.vue';
import AppReview from './components/AppReview.vue';
import AppBlog from './components/AppBlog.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {

    }
  },

  components: {

    AppHeader,
    AppPro,
    AppServices,
    AppShop,
    AppReview,
    AppBlog,
    AppFooter,

  },

}
</script>


<template>

  <div class="relative">

    <AppHeader></AppHeader>
  
    <AppPro></AppPro>
  
    <AppServices></AppServices>
  
    <AppShop></AppShop>
  
    <AppReview></AppReview>
  
    <AppBlog> </AppBlog>

  </div>


  <div class="fixed">

    <AppFooter></AppFooter>

  </div>

</template>


<style lang="scss" scoped>
  
.relative {
  position: relative;
  z-index: 2;
  height: 100%;
  margin-bottom: 460px;
}

.fixed {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 460px;  
}

</style>