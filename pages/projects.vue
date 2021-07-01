<template>
  <div class="projects">
    <Project
        name="Shiganshima Online Clothes Retail Store"
        type="Web Application"
        year="2021"
        :imgSrc="require('~/assets/images/project1.png')"
    />

    <Project
        name="Personal Portfolio"
        type="Webpage"
        year="2021"
        :imgSrc="require('~/assets/images/project2.png')"
    />
  </div>
</template>

<script>
export default {
  head: () => ({
    title: 'My Projects',
  }),
};
</script>

<style lang="scss" scoped>
.projects {
    display: flex;
    flex-direction: row;
    margin-left: 200px;
}
</style>