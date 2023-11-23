<script>
import AppHeader from './components/AppHeader.vue';
import ProductList from './components/ProductList.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    ProductList,
    AppMain,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <ProductList />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>