<template>
  <div id="container">
    <div id="skills">
      <div id="skillsHave">
        <h2>WORKING KNOWLEDGE</h2>
        <ul>
          <li>HTML5</li>
          <li>HTML5</li>
          <li>HTML5</li>
          <li>HTML5</li>
          <li>HTML5</li>
        </ul>
      </div>
      <div id="skillsKnown">
        <h2>KNOW SOMETHING ABOUT</h2>
      </div>
      <div id="skillsToLearn">
        <h2>WANT TO LEARN</h2>
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

span {
  animation-name: fadein;
  animation-duration: 2s;
  animation-iteration-count: initial;
}

#skills {
  width: 100%;
  height: 100%;

  display: grid;
  grid-template-columns: 21% 25% 25% 25%;
  grid-template-rows: auto auto auto;

  #skillsHave {
    // border: 1px solid red;
    width: 200px;
    grid-column-start: 2;

    font-size: 1rem;
    text-align: center;
    
    li {
      list-style: none;
      margin-left: -20%;
    }
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
