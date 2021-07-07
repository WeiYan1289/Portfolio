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
        <div class="the-title">Some Information About Me...... </div>
        <div class="para">
          <p>
            Hi, my name is Wei Yan. I'm a I am <span>Fresh Graduate Software Engineer</span> who 
            seeking a full-time position in the field of IT industry, where I can 
            apply my knowledges and skills for continuous improvement.
          </p>
        </div>
        <div class="para">
          <p>
            For some demographics information about myself, I was born in year <span>1999</span>
            and I come from <span>Tangkak Johor</span>, a place of Johor which nearby Melaka state. 
            It is a small place but full with delicious foods and beautiful scenery.
          </p>
        </div>
        <div class="para">
          <p>
            Before I start my degree in UTAR, I rarely expose to programming and coding
            related stuffs. After getting deeper and deeper about the programming, I found
            that coding are actually <span>interesting</span> as it can achieve almost all the things 
            I want to achieve and the results I want the system to behave. Therefore, <span>I'm
            glad</span> that I chose <span>Software Engineering</span> as my Degree course and I decide to keep
            improving my skills and knowledge to make me more familiar and comfortable while
            coding.  
          </p>
        </div>
        <div class="para">
          <p>
            Although I feel that programming is interesting but sometimes <span>problems</span> and <span>challenges</span>
            will arise while I am dealing with it. While I face problems and challenges while coding, 
            I will google and search for any possible way to overcome it. Besides that, I will watch 
            some videos regarding technologies to strengthen my fundamental and improving 
            my knowledge so I can get more ideas about some projects I would like to start in 
            the future.
          </p>
        </div>
        <div class="para">
          <p>
            Other than technology, I like to play <span>badminton</span> and <span>snooker</span> during my free time. I 
            started to play badminton while I was in my primary school. For snooker, I started to 
            expose it while I come to university.
          </p>
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
        font-size: 1.7em;
        font-weight: 800;
      }
      .para {
        margin-top: 40px;
        font-size: 1.45em;

        > p {
          > span {
            font-weight: bold;
            color: brown;
          }
        }
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
          font-size: 1.4em;
          font-weight: 700;
        }
        .para {
          margin-top: 20px;
          font-size: 1.25em;
        }
      }
    }
  }
}
</style>
