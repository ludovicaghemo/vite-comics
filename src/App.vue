<script>
//importare AppHeader - AppBody - AppFooter
import AppHeader from './components/AppHeader.vue';
import AppBody from './components/AppBody.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';

//dichiarare AppHeader - AppBody - AppFooter
export default {
  components: {
    AppHeader,
    AppBody,
    AppBanner,
    AppFooter,
  },
};
</script>

<template>
<!-- utilizzare AppHeader - AppBody - AppFooter-->
<AppHeader />
<AppBody />
<AppBanner />
<AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
