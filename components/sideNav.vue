<template>
    <div class="side-nav">
        <a class="icon" href="https://www.facebook.com/weiyan.tan.33/" target="_blank">
            <v-icon x-large> mdi-facebook </v-icon>
        </a>
        <a class="icon" href="https://www.linkedin.com/in/wei-yan-tan-945468203/" target="_blank">
            <v-icon x-large> mdi-linkedin</v-icon>
        </a>
        <a class="icon" href="https://www.instagram.com/weiyann_tan/" target="_blank">
            <v-icon x-large> mdi-instagram </v-icon>
        </a>
        <a class="icon" href="https://github.com/WeiYan1289" target="_blank">
            <v-icon x-large> mdi-github </v-icon>
        </a>
    </div>
</template>

<script>
</script>

<style lang="scss" scoped>
.side-nav {
  width: 80px;
  position: fixed;
  left: 0;
  top: 0;
  bottom: 0;
  padding-top: 214px;

  .icon {
    margin: 0 0 21px;
    display: block;
    text-align: center;
    text-decoration: none;
    color: gray;

    :hover {
      color: #C5976B;
    }
  }
}
</style>
