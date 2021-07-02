<template>
  <div class="top-nav">
    <div class="logo">
      <nuxt-link class="nuxt" to="/">
        <img class="logo-img" src="~/assets/images/logo.svg" alt="WY Logo" />
      </nuxt-link>
    </div>
    <div class="wrapper">
      <div class="links">
        <nuxt-link class="nuxt" to="/profile">
          <div class="link" :class="{ 'link-active': isProfile }">
            about me
            <v-icon v-if="isProfile">mdi-folder-account</v-icon>
            <v-icon v-if="isProfile">mdi-card-account-details</v-icon>
          </div>
        </nuxt-link>
        <nuxt-link class="nuxt" to="/education">
          <div class="link" :class="{ 'link-active': isEducation }">
            educations
            <v-icon v-if="isEducation">mdi-school</v-icon>
            <v-icon v-if="isEducation">mdi-book-open-page-variant</v-icon>
          </div>
        </nuxt-link>
        <nuxt-link class="nuxt" to="/projects">
          <div class="link" :class="{ 'link-active': isProjects }">
            projects
            <v-icon v-if="isProjects">mdi-puzzle</v-icon>
            <v-icon v-if="isProjects">mdi-clipboard-text-search</v-icon>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    isProfile() {
      if (this.$route.path == "/profile") {
        return true;
      } else {
        return false;
      }
    },

    isEducation() {
      if (this.$route.path == "/education") {
        return true;
      } else {
        return false;
      }
    },

    isProjects() {
      if (this.$route.path == "/projects") {
        return true;
      } else {
        return false;
      }
    }
  }
};
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
  width: 1000px;
  font-size: 35px;
}
.nuxt {
  text-decoration: none;
}
.link {
  color: #a8a8a8 !important;
  width: 300px;
}
.link-active {
  color: black !important;
}
.v-icon {
  color: black;
}
</style>
