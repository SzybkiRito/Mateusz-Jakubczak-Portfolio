<template>
  <div id="container" class="page">
    <div id="about_container">
      <h1>About Me</h1>
      <div id="text">
        Cześć! Nazywam się Mateusz Jakubczak, mam siedemaście lat i obecnie
        chodzę do trzeciej klasy technikum kinematograficzno-komputerowego im.
        Krzysztofa Kieślowskiego w Warszawie na profil technik-informatyk.
        Uwielbiam jeździć na rowerze i grać w siatkówkę, a w wolnym czasie
        rozwijam się w kierunku Frontend Developera ucząc się coraz to nowszych
        technologie. <br />
        Znajdź mnie: <a href="https://github.com/SzybkiRito">GitHub</a> /
        <a href="https://www.linkedin.com/in/mateusz-jakubczak-1073591b9/"
          >LinkedIn</a
        >
        /
        <a href="https://www.linkedin.com/in/mateusz-jakubczak-1073591b9/"
          >Pracuj.pl</a
        >
      </div>
      <div id="submitButton">
        <button @click="pushToSkills">Skills</button>
      </div>
    </div>
    <div id="projects">
      <div
        id="calculator_project"
        class="project"
        @click="githubLink('https://vue-calculator-szybkirito.herokuapp.com/')"
      >
        <img
          src="~@/assets/calculator.jpg"
          width="250px"
          height="150px"
          id="calculator"
        />
        <span class="project_name">Calculator</span>
      </div>
      <div
        id="fullstack_project"
        class="project"
        @click="githubLink('https://vue-login-panel-webpage.herokuapp.com/#/')"
      >
        <img
          src="~@/assets/fullstack.png"
          width="250px"
          height="150px"
          id="calculator"
        />
        <span class="project_name">Fullstack project with login panel</span>
      </div>
      <div
        id="roleplay_project"
        class="project"
        @click="githubLink('https://vueroleplaywebsite.herokuapp.com/#/')"
      >
        <img
          src="~@/assets/roleplay_website.jpg"
          width="250px"
          height="150px"
          id="calculator"
        />
        <span class="project_name">Roleplay website for a server in game</span>
      </div>
    </div>
  </div>
</template>

<script>
import router from "../router";
export default {
  name: "About",
  methods: {
    githubLink(link) {
      window.open(link, "_blank");
    },
    pushToSkills() {
      router.push('/skills');
    }
  },
};
</script>

<style scoped lang="scss">
a {
  color: white;
}
.particle {
  position: absolute;
  border-radius: 50%;
}
#container {
  overflow-x: hidden;
  width: 100%;
  min-height: 100vh;
  background-color: #1a1a1a;

  display: grid;
  grid-template-columns: auto auto auto;
}

@keyframes fadein {
  0% {
    opacity: 0.0;
  }
  100% {
    opacity: 1.0;
  }
}

#about_container {
  grid-row-start: 2;
  font-family: "Titillium Web", sans-serif;
  color: white;
  max-width: 500px;
  height: 100%;
  h1 {
    margin-left: 2vw;
  }
  #text {
    margin-left: 2vw;
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
    margin: 1vh 2vw;
  }
  button:hover {
    box-shadow: inset 150px 0 2px 0px #ffffff;
    color: black;
  }

  animation-name: fadein;
  animation-duration: 2s;
  animation-iteration-count: initial;

}
#projects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-row-gap: 50px;
  grid-column-start: 2;
  grid-row-start: 2;

  animation-name: fadein;
  animation-duration: 2s;
  animation-iteration-count: initial;

  font-family: "Titillium Web", sans-serif;
  width: 100%;
  height: 150px;
  #calculator {
    border-radius: 15px;
  }
  span {
    text-align: center;
  }
}
#submitButton {
  width: 100%;
}
@media only screen and (max-width: 768px) {
  #about_container {
    margin: 10px;
    grid-row-start: 1;
    text-align: center;
  }
  #projects {
    height: 100%;
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    justify-items: center;
    grid-row-gap: 5px;
    grid-row-start: 2;
    grid-column-start: 1;
  }
}
@media only screen and (max-width: 1200px) {
  #about_container {
    margin: 10px;
    grid-row-start: 1;
    text-align: center;
  }
  #projects {
    height: 100%;
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    justify-items: center;
    grid-row-gap: 5px;
    grid-row-start: 2;
    grid-column-start: 1;
  }
}
#projects {
  -webkit-transition: opacity 1s ease-in-out;
  -moz-transition: opacity 1s ease-in-out;
  -ms-transition: opacity 1s ease-in-out;
  -o-transition: opacity 1s ease-in-out;
  transition: opacity 1s ease-in-out;
}
.project:hover {
  zoom: 1;
  filter: alpha(opacity=40);
  opacity: 0.4;
  box-shadow: white 0px 0px 0px;

  .project_name {
    zoom: 1;
    filter: alpha(opacity=40);
    opacity: 1.0;
    box-shadow: white 0px 0px 0px;
    display: block;
  }
}
.project {
  height: 100%;
  width: 250px;
  // border: 1px solid red;
}
.project_name {
  color: white;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0.0;
}
</style>
