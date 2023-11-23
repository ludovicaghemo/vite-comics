<script>
//importare AppHeader - AppBody
import AppHeader from './components/AppHeader.vue';
import AppBody from './components/AppBody.vue';

//dichiarare AppHeader
export default {
  components: {
    AppHeader,
    AppBody,
  },
};
</script>

<template>
<!-- utilizzare AppHeader -->
<AppHeader />
<AppBody />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
