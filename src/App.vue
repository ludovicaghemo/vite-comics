<script>
//importare AppHeader - AppBody - AppFooter
import AppHeader from './components/AppHeader.vue';
import AppBody from './components/AppBody.vue';
import AppFooter from './components/AppFooter.vue';

//dichiarare AppHeader - AppBody - AppFooter
export default {
  components: {
    AppHeader,
    AppBody,
    AppFooter,
  },
};
</script>

<template>
<!-- utilizzare AppHeader - AppBody - AppFooter-->
<AppHeader />
<AppBody />
<AppFooter />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
