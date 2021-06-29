<template>
    <div class="top-nav">
        <div class="logo">
            <a class="icon" href="https://www.google.com/" target="_blank">
            <img
                class="logo-img"
                src="~/assets/images/logo.svg"
                alt="WY Logo"
            />
        </a>
        </div>
        <div class="wrapper">
            <div class="links">
            <nuxt-link class="nuxt" to="/profile">
                <div class="link" :class="{ 'link-active': isProfile }">about me</div>
            </nuxt-link>
            <nuxt-link class="nuxt" to="/education">
                <div class="link" :class="{ 'link-active': isEducation }">educations</div>
            </nuxt-link>
            <nuxt-link class="nuxt" to="/project">
                <div class="link" :class="{ 'link-active': isProject }">projects</div>
            </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  computed: {
    isProfile() {
      if(this.$route.path == "/profile"){
        return true;
      }
      else{
        return false;
      }
    },

    isEducation() {
    if(this.$route.path == "/education"){
        return true;
      }
      else{
        return false;
      }
    },
    
    isProject() {
    if(this.$route.path == "/project"){
        return true;
      }
      else{
        return false;
      }
    },
  }
}
</script>

<style lang="scss" scoped>
.top-nav {
  margin-left: 80px;
  display: flex;
  justify-content: space-between;
  width: 50%;

  .wrapper {
    margin: 110px 0;
  }
}
.links {
  display: flex;
  justify-content: space-between;
  width: 800px;
  font-size: 35px;
}
.nuxt {
  text-decoration: none;
}
.link {
  color: black !important;
}
.link-active {
  color: red !important;
}
</style>
