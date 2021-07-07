<template>
  <div class="profile">
    <div class="profile-container">
      <div class="profile-container-left">
        <img
          class="my-photo"
          src="~/assets/images/profile.jpg"
          alt="my avatar"
        />
      </div>
      <div class="profile-container-right">
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

  .profile-container {
    display: flex;

    .profile-container-left {
      padding: 30px;
    }

    .profile-container-right {
      max-width:700px;
      padding-top: 30px;

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

@media screen and (min-width: 1000px) {
  .profile {
    margin: 0 20%;

    .profile-container {
      width: 80vw;
    }

    .profile-container-right {
      margin-left: 50px;
    }
  }
}

@media screen and (max-width: 1000px) {
  .profile {
    margin: 0 10%;
    
    .profile-container {
      flex-direction: column;
      align-items: center;

      .profile-container-right {
        padding-top: 0;

        .the-title {
          font-size: 1.5em;
          font-weight: 700;
        }
        .para {
          margin-top: 20px;
          font-size: 1.3em;
        }
      }
    }
  }
}
</style>
