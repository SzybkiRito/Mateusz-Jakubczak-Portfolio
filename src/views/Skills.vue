<template>
  <div id="container">
    <div id="skills">
      <div id="skillsHave">
        <h2>WORKING KNOWLEDGE</h2>
        <ul>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>CSS Grid</li>
          <li>CSS FlexBox</li>
          <li>Vue.js</li>
          <li>Node.js</li>
          <li>Responsive Web Design</li>
        </ul>
      </div>
      <div id="skillsKnown">
        <h2>KNOW SOMETHING ABOUT</h2>
        <ul>
          <li>SASS</li>
          <li>Working with API</li>
          <li>Express</li>
          <li>Git</li>
        </ul>
      </div>
      <div id="skillsToLearn">
        <h2>WANT TO LEARN</h2>
        <ul>
          <li>Typescript</li>
          <li>React JS</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills",
};
</script>

<style scoped lang="scss">
#container {
  overflow-x: hidden;
  width: 100%;
  min-height: 100vh;
  background-color: #1a1a1a;
  font-family: "Titillium Web", sans-serif;
  color: white;
}

#skillsToLearn,
#skillsKnown,
#skillsHave {
  // border: 1px solid red;
  margin-top: 20px;
  margin-left: auto;
  margin-right: auto;

  width: 200px;
  font-size: 1rem;
  text-align: center;

  li {
    list-style: none;
    margin-left: -20%;
  }

  animation-name: fadein;
  animation-duration: 2s;
  animation-iteration-count: initial;
}

#skills {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;

  #skillsHave {
  }
}

@keyframes fadein {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
