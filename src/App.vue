<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import IconsList from './components/IconsList.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    IconsList
}
}
</script>

<template>
    <AppHeader />
    <AppMain />
    <IconsList />
    <AppFooter />
</template>

<style lang="scss">

</style>