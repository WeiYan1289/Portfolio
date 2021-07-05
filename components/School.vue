<template>
  <div class="school">
    <div class="school-container">
        <div class="school-container-left">
            <img class="school-img" :src="imgSrc" :alt="name" />
        </div>
        <div class="school-container-right">
            <div class="name">
                <span>
                    {{ name }} <span>({{ year }})</span>
                </span>
            </div>
            <div class="field">{{ scholar }} — {{ field }}</div>
            <div class="result">{{ result }}
                <div class="emph"></div>
            </div>
            <slot>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eveniet
                    quod nostrum dolore ipsam blanditiis repellendus cum maiores facilis,
                    laudantium accusantium quasi perferendis. Facilis minima eligendi
                    cupiditate ipsum similique commodi!
                </p>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eveniet
                    quod nostrum dolore ipsam blanditiis repellendus cum maiores facilis,
                    laudantium accusantium quasi perferendis. Facilis minima eligendi
                    cupiditate ipsum similique commodi!
                </p>
            </slot>
        </div>
    </div>
  </div>
</template>

<script>
export default{
  props: {
    name: { type: String, default: '' },
    year: { type: String, default: '' },
    scholar: { type: String, default: '' },
    field: { type: String, default: '' },
    result: { type: String, default: '' },
    imgSrc: { type: String, default: '' },
  },
}
</script>

<style lang="scss" scoped>
.school {
    display: flex;
    justify-content: flex-start;

    .school-container {
        display: flex;

        .school-container-left {
            .school-img {
                max-width: 400px;
                min-height: 300px;
                margin: 30px;
                box-shadow: 0px 3px 5px 2px gray !important;;
            }
        }
        
        .school-container-right {
            padding-top: 30px;

            .name {
                > span {
                    font-size: 1.6em;
                    font-weight: bold;
                    > span {
                        color: gray !important;
                        font-weight: normal !important;
                    }
                }
            }

            .field {
                font-size: 1.2em;
            }

            .result {
                font-size: 1.4em;
                width: fit-content;
                .emph {
                    content: '';
                    margin-left: 3px;
                    height: 5px;
                    background: brown;
                }
            }

            > p {
                margin-top: 15px;
                margin-bottom: 25px;
                font-size: 1.45em;
            }
        }
    }
}

@media screen and (min-width: 1000px) {
  .school {
    margin: 0 17.5%;

    .school-container {
      width: 80vw;
    }
  }
}

@media screen and (max-width: 1000px) {
  .school {
    margin: 0 10%;
    
    .school-container {
      flex-direction: column;
      align-items: center;

      .school-container-left {
        .school-img {
            max-width: 80vw;
            height: auto;
            margin: 0;
            box-shadow: 0px 3px 5px 2px gray !important;;
        }
      }

      .school-container-right {
        padding-top: 10px;
        padding-bottom: 45px;

        .name {
            > span {
                font-size: 1.4em;
            }
        }
        
        .field {
            font-size: 1em;
        }

        .result {
            font-size: 1.2em;
        }

        > p {
          font-size: 1.25em;
        }
      }
    }
  }
}
</style>