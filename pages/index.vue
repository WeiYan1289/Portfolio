<template>
  <div class="home">
    <span>Welcome to Wei Yan's Portfolio</span>
    <div class="content">
        <div class="slider-wrapper">
            <div class="slider">
                <div class="slider-text1">Hello</div>
                <div class="slider-text2">Bonjour</div>
                <div class="slider-text3">Olá</div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  head: () => ({
    title: 'Welcome to my Portfolio',
  }),
};
</script>

<style lang="scss" scoped>
.home {
  text-align: center;
  width: 100%;
  margin-top: 120px;

  > span{
    font-size: 4em;
    font-weight: bold;
  }
}

.content {
    margin-top: 50px;
}


.slider-wrapper {
    font-size: 40px;
    color: #aaa;
    font-weight: bold;
    text-transform: uppercase;
    display: flex;
    align-items: center;
    justify-content: center;
}
.slider {
    height: 50px;
    overflow: hidden;
}
.slider div {
    color: #fff;
    height: 50px;
    margin-bottom: 50px;
    padding: 2px 15px;
    text-align: center;
}
.slider-text1 {
    background: lightgreen;
    animation: slide 6s linear infinite;
}
.slider-text2 {
    background: skyblue;
}
.slider-text3 {
    background: lightcoral;
}
@keyframes slide {
    0% {margin-top: -300px;}
    5% {margin-top: -200px;}
    33% {margin-top: -200px;}
    38% {margin-top: -100px;}
    66% {margin-top: -100px;}
    71% {margin-top: 0px;}
    100% {margin-top: 0px;}
}

@media screen and (max-width: 1000px) {
  .home{
    margin-top:40%;

    > span{
      font-size: 3em;
    }
  }
}
</style>