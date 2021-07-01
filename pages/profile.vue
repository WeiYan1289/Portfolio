<template>
  <div class="profile">
    <img class="my-photo" src="~/assets/images/profile.jpg" alt="my avatar" />
    <div class="intro">
      <span>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eveniet
        quod nostrum dolore ipsam blanditiis repellendus cum maiores facilis,
        laudantium accusantium quasi perferendis. Facilis minima eligendi
        cupiditate ipsum similique commodi!
      </span>
    </div>
  </div>
</template>

<script>
export default {
  head: () => ({
    title: 'My Profile',
  }),
};
</script>

<style lang="scss" scoped>
.profile {
    display: flex;
    flex-direction: row;
    margin-left: 200px;
}

.my-photo {
  max-width: 250px;
  max-height: 250px;
  border-radius: 40%;
}

.intro {
  margin: 0 5%;
}
</style>
