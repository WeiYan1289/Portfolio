<template>
  <div class="school">
    <img class="school-img" :src="imgSrc" :alt="name" />
    <div class="school-content">
      <div class="school-content-name">
        <span>
          {{ name }} <span>({{ year }})</span>
        </span>
      </div>
      <div class="school-content-field">{{ scholar }} — {{ field }}</div>
      <div class="school-content-result">{{ result }}
          <div class="emph"></div>
      </div>
      
      <slot>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eveniet
          quod nostrum dolore ipsam blanditiis repellendus cum maiores facilis,
          laudantium accusantium quasi perferendis. Facilis minima eligendi
          cupiditate ipsum similique commodi!
        </p>
      </slot>
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
    flex-direction: column;
    padding-right: 15%;

    .school-img {
        max-width: 400px;
        min-height: 300px;
        box-shadow: 0px 3px 5px 2px gray !important;;
    }

    .school-content {
        margin-top: 10px;

        .school-content-name {
            > span {
                font-size: 1.4em;
                font-weight: bold;

                > span {
                    color: gray !important;
                    font-size: 0.75em !important;
                    font-weight: normal !important;
                }
            }
        }

        .school-content-field {
            font-size: 1.15em;
        }

        .school-content-result {
            position: relative;
            width: fit-content;

            .emph {
                content: '';
                position: absolute;
                bottom: -6px;
                left: 3px;
                right: -5px;
                height: 5px;
                background: brown;
            }
        }
    }
}
</style>