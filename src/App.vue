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

  <AppHeader></AppHeader>

  <AppPro></AppPro>

  <AppServices></AppServices>

  <AppShop></AppShop>

  <AppReview></AppReview>

  <AppBlog></AppBlog>

  <AppFooter></AppFooter>

</template>


<style lang="scss" scoped>
  


</style>