<template>
  <div id="app">
    <main>
        <div class="block-lg">
          <div class="block-sm block-sm__content-parent">
            <h1>DOOS & KOOKER</h1>
            <p>Funk forged in Valhalla delivered by two hot-headed dutchmen. Join our journey into this jazzy abyss by surrendering to the swingin’ soul shattering sounds of DOOS & KOOKER.</p>
          </div>
          <div class="block-sm block-sm__content-parent">
            <img src="/img/vinyl.svg" alt="clipart vinyl">
          </div>
          <div class="block-sm">
            <div class="block-tny"></div>
            <div class="block-tny block-tny__content-parent"><img src="/img/thing.svg" alt="volume knob animation" ></div>
            <a class="block-tny block-tny--full-width block-tny--inverted" href="mailto:bookings@doosandkooker.com">CONTACT</a>
          </div>
          <div class="block-sm">
            <img style="border-right: none;" class="block-tny block-tny--full-width" src="/img/halves.svg" alt="circle halves bauhaus animation" >
            <!-- <div class="block-tny block-tny--full-width"></div> -->
            <div class="block-tny"></div>
            <img class="block-tny" src="/img/wave.svg" alt="animated wave graphic" >
          </div>
        </div>
        <div class="block-lg">
          <div class="block-sm">
            <div class="block-tny"><img src="/img/square.svg" alt="transparent square with thick border" ></div>
            <div class="block-tny"></div>
            <div class="block-tny block-tny--full-width block-tny__content-parent"><h2>Unshaven, unaware and incomprehensible.</h2></div>
          </div>
          <img class="block-sm" src="/img/K.webp" alt="headshot KOOKER" onerror="this.onerror=null; this.src='/img/K.png'">
          <img class="block-sm" src="/img/D.jpg" alt="DOOS drinking coffee" >
          <div class="block-sm">
            <div class="block-tny"></div>
            <a class="block-tny block-tny--inverted" href="https://herres.haus"><h1>HH</h1></a>
            <img class="block-tny" src="/img/circle.svg" alt="" >
            <div class="block-tny"></div>
          </div>
        </div>
    </main>
    <footer>
      <div>✔︎ Developed in-house by <a href="https://willwillems.com">this guy</a>.</div>
    </footer>
    <div class="swiss-overlay"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
:root {
  --main-color: #E5AC6F;
  --base-color: black;
}

* {
  box-sizing: border-box;
}

html, body {
  height: 100%;
  width: 100%;
  margin: 0;
  background-color: var(--main-color);
  color: var(--base-color);
}

body {
  text-transform: uppercase;
  padding: 48px 12px;
}

#app {
  font-family: Arial, sans-serif;
  font-weight: 800;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1, h2, h3, h4, h5, h6 {
  font-family: "Arial Black", Arial, sans-serif;
  font-weight: 900;
  line-height: 1em;
  margin: .25em 0;
}

p {
  margin: .75em 0;
  line-height: 1.35em;
}

main {
  border: 1px solid var(--base-color);
  display: grid;
  grid-template-columns: repeat(2, 680px);
  grid-template-rows: repeat(1, 680px);
}
@media only screen and (max-width: 1080px) {
  main {
    grid-template-columns: repeat(1, 1fr);
    grid-template-rows: repeat(2, 1fr);
  }
}


.block-lg {
  display: grid;
  grid-template-columns: repeat(2, 340px);
  grid-template-rows: repeat(2, 340px);
  border: none;
}
@media only screen and (max-width: 680px) {
  .block-lg {
    grid-template-columns: repeat(1, 1fr);
    grid-template-rows: repeat(4, 1fr);
  }
}

.block-sm {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  align-content: center;

  border: 1px solid var(--base-color);
  height: 340px;
  width: 340px;

  object-fit: cover;
}

.block-sm__content-parent {
  padding: 24px 48px;
}

.block-tny {
  height: 171px;
  width: 171px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  object-fit: cover;

  /* text-align: center; */
  line-height: 160px;

  border: 1px solid var(--base-color);
  margin: -1px;

  transition: transform .3s ease-out;
}

.block-tny__content-parent {
  padding: 24px 48px;

}

.block-tny--full-width {
  width: 340px;
}

.block-tny--inverted {
  color: var(--main-color);
  background-color: var(--base-color);
}

a.block-tny {
  font-size: 2rem;
  letter-spacing: 2px;
  text-decoration: none;
}

a.block-tny:hover {
  transform: scale(1.1);
  background-color: #964141;
  z-index: 1;
}

img {
  max-width: 100%;
  max-height: 100%;

  filter: saturate(1.15); /* temp fix! */
}

img:hover {
  filter: saturate(1.15) hue-rotate(-6deg);
}

footer {
  padding: 24px 12px;
}

footer a {
  color: black;
}

.swiss-overlay {
  pointer-events: none;

  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;

  background-image: url('/img/noise.jpg');
  opacity: 0.06;
}

</style>
