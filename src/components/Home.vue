<template>
  <div id="container">
    <LoadingScreen v-if="show" class="loadingscreen" />
    <div class="particles" v-if="!show">
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
    </div>
    <div class="main_page_text" v-if="!show">
      Mateusz Jakubczak
      <span
        ><strong>Front-End <span id="color">Developer</span></strong></span
      >
      <button @click="showLoadingScreen()">About Me</button>
    </div>
  </div>
</template>

<script>
import LoadingScreen from "@/components/LoadingScreen.vue";
import router from "../router";
export default {
  name: "Home",
  components: {
    LoadingScreen
  },
  data() {
    return {
      show: false
    };
  },
  methods: {
    showLoadingScreen() {
      this.show = true;
      setTimeout(() => {
        this.show = false;
        router.push('/about')
      }, 2000);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#container {
  overflow: hidden;
  background-color: #1a1a1a;
  height: 100vh;

  display: grid;
  grid-template-columns: 10% 25% 25% 25%;
  grid-template-rows: auto;
}

.particle {
  position: absolute;
  border-radius: 50%;
}
.main_page_text {
  width: 350px;
  grid-row-start: 2;
  grid-column-start: 2;
  line-height: 35pt;

  font-family: "Titillium Web", sans-serif;
  font-size: 35px;
  color: white;

  span {
    font-family: "Titillium Web", sans-serif;
  }

  #color {
    color: #ab18b8;
  }

  button {
    height: 50px;
    width: 150px;
    outline: none;
    border: none;
    border-radius: 5px;
    background-color: #ab18b8;
    color: white;
    box-shadow: inset 0 0 0 0 #ab18b8;
    -webkit-transition: ease-out 0.4s;
    -moz-transition: ease-out 0.4s;
    transition: ease-out 0.4s;
  }
  button:hover {
    box-shadow: inset 150px 0 0 0 #ffffff;
    color: black;
  }
}
.loadingscreen {
  grid-row-start: 2;
  grid-column-start: 3;
}

@for $i from 1 through 30 {
  @keyframes particle-animation-#{$i} {
    100% {
      transform: translate3d(
        (random(90) * 1vw),
        (random(90) * 1vh),
        (random(100) * 1px)
      );
    }
  }

  .particle:nth-child(#{$i}) {
    animation: particle-animation-#{$i} 60s infinite;
    $size: random(5) + 5 + px;
    opacity: random(100) / 100;
    height: $size;
    width: $size;
    animation-delay: -$i * 0.2s;
    transform: translate3d(
      (random(90) * 1vw),
      (random(90) * 1vh),
      (random(100) * 1px)
    );
    background: hsl(random(360), 70%, 50%);
  }
}
</style>
