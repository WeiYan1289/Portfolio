<template>
  <div class="top-nav">
    <div class="logo">
      <nuxt-link class="nuxt" to="/">
        <img class="logo-img" src="~/assets/images/logo.svg" alt="WY Logo" />
      </nuxt-link>
    </div>
    <div class="burger-placeholder" @click="openSideNav"></div>
    <div class="wrapper" ref="wrapper" @click="closeSideNav">
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
  },
  methods: {
    openSideNav() {
      this.$refs.wrapper.classList.add("pulled-in");
    },
    closeSideNav() {
      this.$refs.wrapper.classList.remove("pulled-in");
    }
  }
};
</script>

<style lang="scss" scoped>
.top-nav {
  display: flex;
  justify-content: space-between;
  width: 100%;
  background: #eee;
  align-items: center;
  padding: 0 80px;

  .wrapper {
    margin: 110px 0;
  }
}
.burger-placeholder {
  display: none;
  height: 40px;
  width: 40px;
  background: gray;
  cursor: pointer;
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

@media screen and (max-width: 1128px) {
}

@media screen and (max-width: 768px) {
}

@media screen and (max-width: 1000px) {
  .top-nav {
    .burger-placeholder {
      display: block;
    }
    .wrapper {
      margin: 0;
      height: 100vh;
      background: pink;
      width: 200px;
      position: fixed;
      top: 0;
      right: 0;
      transition: transform 0.2s ease;
      transform: translateX(100%);

      .links {
        justify-content: space-around;
        height: 40vh;
        width: 100%;
        flex-direction: column;
      }

      &.pulled-in {
        transform: translateX(0);
      }
    }
  }
}

@media screen and (max-width: 1366px) {
  .top-nav {
    .logo-img {
      width: 200px;
    }
  }
}
</style>
