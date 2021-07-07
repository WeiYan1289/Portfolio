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
  position: fixed;
  left: 0;
  bottom: 0;

  .icon {
    text-align: center;
    text-decoration: none;
    color: #686868;
    margin: 0 0 21px;
    display: block;
  }

  :hover {
    color: black;
  }
}
@media screen and (min-width: 1000px) {
    .side-nav {
        width: 80px;
        top: 0;
        padding-top: 264px;
    }
}

@media screen and (max-width: 1000px) {
 .side-nav { 
    width: 100%;
    background: #fbfaf5;
    height: 45px;
    display: flex;
    justify-content: space-between;
    padding: 2.5px 15%;
 }
}
</style>
