<template>
  <div class="project">
    <div class="project-container">
        <div class="project-container-left">
            <div class="title">
                <span>{{ name }}</span>
            </div>
            <div class="subtitle">
                <span>
                {{ type }} <span>({{ year }})</span>
                </span>
            </div>
            <img class="project-img" :src="imgSrc" :alt="name" />
        </div>
        <div class="project-container-right">
            <div class="para">
                <slot>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eveniet
                        quod nostrum dolore ipsam blanditiis repellendus cum maiores facilis,
                        laudantium accusantium quasi perferendis. Facilis minima eligendi
                        cupiditate ipsum similique commodi!
                    </p>
                </slot>
            </div>
            <div class=tech-title>Technology</div>
            <div class="technology">
                <div class="item" v-for="(tech, index) in lists" :key="index">
                    <img class="item-img" :src="tech.imgSrc" />
                    <span>{{ tech.name }}</span>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default{
  props: {
    name: { type: String, default: '' },
    type: { type: String, default: '' },
    year: { type: String, default: '' },
    imgSrc: { type: String, default: '' },
    lists: { type: Array, default: '' }
  },
}
</script>

<style lang="scss" scoped>
.project {
    display: flex;
    justify-content: flex-start;

    .project-container {
        display: flex;

        .project-container-left {
            margin: 30px;

            .title {
                font-size: 1.6em;
                font-weight: bold;
                max-width: 400px;
            }

            .subtitle {
                color: gray !important;
                > span {
                    font-size: 1.3em;
                }
            }

            .project-img {
                max-width: 400px;
                box-shadow: 0px 3px 5px 2px gray !important;;
            }
        }

        .project-container-right {
            max-width: 700px;

            .para {
                font-size: 1.25em;

                >p {
                    margin-bottom: 10px;
                    > span {
                        font-weight: bold!important;
                        color: brown!important;
                    }
                }
            }

            .tech-title {
                font-size: 1.3em;
                font-weight: bold;
                padding: 10px 0;
            }
            .technology {
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                align-items: center;

                .item {
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    margin: 10px 20px;
                    padding: 2.5px 0;
                    text-align: center;

                    .item-img {
                        height: 42px;
                        max-width: 60px;
                    }

                    > span {
                        margin-top: 15px;
                        font-size: 1.1em;
                    }
                }
            }
        }
    }
}

@media screen and (min-width: 1000px) {
  .project {
    margin: 0 17.5%;

    .project-container {
      width: 80vw;

      .project-container-right {
          margin: 100px 0 50px 30px;

          .technology {
              .item {
                  padding: 2.5px 10px;
              }
          }
      }
    }
  }
}

@media screen and (max-width: 1000px) {
  .project {
    margin: 30px 10%;
    
    .project-container {
      flex-direction: column;
      align-items: center;

      .project-container-left {
        margin: 0;
        .title {
            font-size: 1.4em;
        }
        .subtitle {
            font-size: 1em;
        }
        .project-img {
            max-width: 80vw;
            margin: 0;
            box-shadow: 0px 3px 5px 2px gray !important;;
        }
      }

      .project-container-right {
        padding-top: 30px;

        .para {
          font-size: 1.1em;
        }

        .tech-title {
          font-size: 1.2em;
        }
      }
    }
  }
}
</style>