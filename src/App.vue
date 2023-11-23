<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppFooter from './components/AppFooter.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    ProductList,
    AppFooter,
    AppMain
  }
}
</script>

<template>
  <AppHeader />
  <ProductList />
  <AppFooter />
  <AppMain />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>