<template>
  <div class="profile">
    <div class="profile__container">
      <div class="profile__container__left">
        <img
          class="my-photo"
          src="~/assets/images/profile.jpg"
          alt="my avatar"
        />
      </div>
      <div class="profile__container__right">
        <div class="the-title">Hello, my name Wei Yan!</div>
        <div class="para">
          <span>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
            eveniet quod nostrum dolore ipsam blanditiis repellendus cum maiores
            facilis, laudantium accusantium quasi perferendis. Facilis minima
            eligendi cupiditate ipsum similique commodi!
          </span>
        </div>
        <div class="para">
          <span>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
            eveniet quod nostrum dolore ipsam blanditiis repellendus cum maiores
            facilis, laudantium accusantium quasi perferendis. Facilis minima
            eligendi cupiditate ipsum similique commodi!
          </span>
        </div>
        <div class="para">
          <span>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
            eveniet quod nostrum dolore ipsam blanditiis repellendus cum maiores
            facilis, laudantium accusantium quasi perferendis. Facilis minima
            eligendi cupiditate ipsum similique commodi!
          </span>
        </div>
        <div class="para">
          <span>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis
            eveniet quod nostrum dolore ipsam blanditiis repellendus cum maiores
            facilis, laudantium accusantium quasi perferendis. Facilis minima
            eligendi cupiditate ipsum similique commodi!
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head: () => ({
    title: "My Profile"
  })
};
</script>

<style lang="scss" scoped>
.profile {
  display: flex;
  justify-content: flex-start;
  margin-left: 200px;

  &__container {
    display: flex;
    width: 50vw;

    &__left {
      padding: 30px;
    }

    &__right {
      padding-top: 30px;
      margin-left: 50px;
      .the-title {
        font-size: 2em;
        font-weight: 800;
      }
      .para {
        margin-top: 40px;
        font-size: 1.75em;
      }
    }
  }
}

.my-photo {
  max-width: 250px;
  max-height: 250px;
}

.intro {
  margin: 0 5%;
}
</style>
