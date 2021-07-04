<template>
  <div class="my-layout">
    <!-- header -->
    <TopNavigation />
    <div class="my-content">
      <Nuxt />
    </div>
    <SideNavigation />
    <!-- footer -->
  </div>
</template>

<script>
export default {};
</script>

<style>
html {
  font-family: 'Alegreya Sans', sans-serif;
}

.my-content {
  margin-bottom: 60px;
}

.my-layout {
  overflow: hidden;
  min-height: 100vh;
  width: 100vw;
  position: relative;
}
</style>
