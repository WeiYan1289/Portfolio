<template>
  <div class="project">
    <div class="project-title">
        <span>{{ name }}</span>
    </div>
    <div class="project-subtitle">
        <span>
          {{ type }} <span>({{ year }})</span>
        </span>
    </div>
    <img class="project-img" :src="imgSrc" :alt="name" />
  </div>
</template>

<script>
export default{
  props: {
    name: { type: String, default: '' },
    type: { type: String, default: '' },
    year: { type: String, default: '' },
    imgSrc: { type: String, default: '' }
  },
}
</script>

<style lang="scss" scoped>
.project {
    display: flex;
    flex-direction: column;
    padding-right: 15%;

    .project-title {
        font-size: 1.4em;
    }

    .project-subtitle {
        color: gray !important;
        > span {
            font-size: 1em;
            > span {
                font-size: 1.15em !important;
            }
        }
    }

    .project-img {
        max-width: 400px;
        box-shadow: 0px 3px 5px 2px gray !important;;
    }
}
</style>