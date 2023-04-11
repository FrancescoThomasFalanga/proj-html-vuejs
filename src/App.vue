<script>
import AppHeader from './components/AppHeader.vue';
import AppPro from './components/AppPro.vue';
import AppServices from './components/AppServices.vue';
import AppShop from './components/AppShop.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  data() {
    return {

    }
  },

  components: {

    AppHeader,
    AppFooter,
    AppPro,
    AppServices,
    AppShop,

  },

}
</script>


<template>

  <AppHeader></AppHeader>

  <AppPro></AppPro>

  <AppServices></AppServices>

  <AppShop></AppShop>

  <AppFooter></AppFooter>

</template>


<style lang="scss" scoped>
  


</style>