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

    <div class="contact-form">
      <h1>Contact Me</h1>
      <div id="line"></div>
      <form class="form">
        <input required type="text" name="name" placeholder="Name" />
        <input required type="text" name="name" placeholder="E-mail" />
			  <textarea name="message" id="message" rows="4" placeholder="Message"></textarea>

        <button type="submit" class="btn effect04" data-sm-link-text="SEND!">
          <span>CLICK</span>
        </button>
      </form>
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
  min-width: 100%;
  background-color: #1a1a1a;
  font-family: "Titillium Web", sans-serif;
  color: white;

  // display: grid;
  // grid-template-rows: 25% 25% 25% 25%;
}
.contact-form {
  // border: 1px solid red;
  // grid-row-start: 3;

  text-align: center;
  font-family: 16px;
  margin: 0 auto;
  max-width: 600px;
  width: 100%;

  input, #message {
    font-family: Arial, Helvetica, sans-serif;
    padding: 20px;
    margin-bottom: 25px;
    border: none;
    outline: none;
    border-radius: 15px;
    min-width: 300px;
    max-width: 400px;
  }
}
.btn {
  letter-spacing: 0.1em;
  cursor: pointer;
  font-size: 14px;
  font-weight: 400;
  line-height: 45px;
  max-width: 160px;
  position: relative;
  text-decoration: none;
  text-transform: uppercase;
  width: 100%;
  background-color: rgb(208, 114, 14);
  color: white;
  border: none;
  outline: none;
  text-align: center;
}
.btn:hover {
  text-decoration: none;
}
.effect04 {
  --uismLinkDisplay: var(--smLinkDisplay, inline-flex);
  display: var(--uismLinkDisplay);
  color: #000;
  outline: solid 2px #000;
  position: relative;
  transition-duration: 0.4s;
  overflow: hidden;
}
.effect04::before,
.effect04 span {
  margin: 0 auto;
  transition-timing-function: cubic-bezier(0.86, 0, 0.07, 1);
  transition-duration: 0.4s;
}
.effect04:hover {
  background-color: #000;
}
.effect04:hover span {
  -webkit-transform: translateY(-400%) scale(-0.1, 20);
  transform: translateY(-400%) scale(-0.1, 20);
}
.effect04::before {
  content: attr(data-sm-link-text);
  color: #fff;
  position: absolute;
  left: 0;
  right: 0;
  margin: auto;
  -webkit-transform: translateY(500%) scale(-0.1, 20);
  transform: translateY(500%) scale(-0.1, 20);
}
.effect04:hover::before {
  letter-spacing: 0.05em;
  -webkit-transform: translateY(0) scale(1, 1);
  transform: translateY(0) scale(1, 1);
}
.contact-form .form {
  display: flex;
  align-items: center;
  flex-direction: column;
  font-size: 16px;
}
#line {
  max-width: 80%;
  margin: 0 auto;
  border-bottom: solid 1px rgb(208, 114, 14);
  margin-top: -20px;
  opacity: 0.3;
  margin-bottom: 15px;
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
