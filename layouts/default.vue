<template>
  <div class="my-layout">
    <!-- header -->
    <SideNavigation />
    <TopNavigation />
    <Nuxt />
    <!-- footer -->
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.my-layout {
  overflow: hidden;
  min-height: 100vh;
  width: 100vw;
  position: relative;
}
</style>
