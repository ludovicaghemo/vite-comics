<script>
//importare AppHeader - AppBody - AppFooter
import AppHeader from './components/AppHeader.vue';
import AppBody from './components/AppBody.vue';
import AppCard from './components/AppCard.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';

//dichiarare AppHeader - AppBody - AppFooter
export default {
  components: {
    AppHeader,
    AppBody,
    AppCard,
    AppBanner,
    AppFooter,
  },
};
</script>

<template>
<!-- utilizzare AppHeader - AppBody - AppFooter-->
<AppHeader />
<AppBody />
<AppCard />
<AppBanner />
<AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
