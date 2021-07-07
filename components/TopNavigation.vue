<template>
  <div class="top-nav">
    <div class="logo">
      <nuxt-link class="nuxt" to="/">
        <img class="logo-img" src="~/assets/images/logo.png" alt="WY Logo" />
      </nuxt-link>
    </div>
    <div class="burger-placeholder" @click="openSideNav">
        <v-icon x-large>mdi-backburger</v-icon>
    </div>
    <div class="wrapper" ref="wrapper" @click="closeSideNav">
      <div class="links">
        <nuxt-link class="nuxt" to="/profile">
          <div class="link" :class="{ 'link-active': isProfile }">
            About Me
            <v-icon v-if="isProfile">mdi-folder-account</v-icon>
            <v-icon class="deco-btn" v-if="isProfile">mdi-card-account-details</v-icon>
          </div>
        </nuxt-link>
        <nuxt-link class="nuxt" to="/education">
          <div class="link" :class="{ 'link-active': isEducation }">
            Educations
            <v-icon v-if="isEducation">mdi-school</v-icon>
            <v-icon class="deco-btn" v-if="isEducation">mdi-book-open-page-variant</v-icon>
          </div>
        </nuxt-link>
        <nuxt-link class="nuxt" to="/projects">
          <div class="link" :class="{ 'link-active': isProjects }">
            Projects
             <v-icon v-if="isProjects">mdi-clipboard-text-search</v-icon>
            <v-icon class="deco-btn" v-if="isProjects">mdi-puzzle</v-icon>
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
      return this.$route.path == "/profile";
    },

    isEducation() {
      return this.$route.path == "/education";
    },

    isProjects() {
      return this.$route.path == "/projects";
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
  background: #fbfaf5;
  align-items: center;
  padding: 0 80px;

  .wrapper {
    margin: 110px 0;
  }
}
.logo-img {
  max-width: 200px;
}
.burger-placeholder {
  display: none;
  height: 40px;
  width: 40px;
  cursor: pointer;
}
.links {
  display: flex;
  justify-content: space-between;
  width: 1000px;
  font-size: 32px;
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

@media screen and (max-width: 1150px) {
  .top-nav {
    padding-left: 10px;
    padding-right: 30px;
    
    .burger-placeholder {
      display: block;
    }

    .deco-btn {
      visibility: hidden;
    }

    .wrapper {
      margin: 0;
      height: 100vh;
      background: #EFEFEF;
      width: 200px;
      position: fixed;
      top: 0;
      right: 0;
      transition: transform 0.2s ease;
      transform: translateX(100%);
      border-left: #eee solid 1px;
      padding-left: 15px;

      .links {
        justify-content: space-around;
        height: 40vh;
        max-height: 300px;
        width: 100%;
        flex-direction: column;
        font-size: 26px !important;
      }

      &.pulled-in {
        transform: translateX(0);
      }
    }
  }
}
</style>
