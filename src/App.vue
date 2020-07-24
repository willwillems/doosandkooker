<template>
  <div id="app">
    <main>
        <div class="block-lg">
          <div class="block-sm block-sm__content-parent">
            <h1>DOOS & KOOKER</h1>
            <p>Funk forged in valhalla by two hot-headed dutchmen. Join the journey into this jazzy abbys by surrendering to the swingin’ soul shattering sounds of DOOS & KOOKER.</p>
          </div>
          <div class="block-sm block-sm__content-parent">
            <img src="/img/vinyl.svg" alt="">
          </div>
          <div class="block-sm">
            <div class="block-tny">ggg</div>
            <div class="block-tny block-tny__content-parent"><img src="/img/thing.svg" alt="" ></div>
            <a class="block-tny block-tny--full-width block-tny--inverted">CONTACT</a>
          </div>
          <div class="block-sm">
            <div class="block-tny block-tny--full-width">ggg</div>
            <div class="block-tny">ggg</div>
            <div class="block-tny">ggg</div>
          </div>
        </div>
        <div class="block-lg">
          <div class="block-sm">
            <div class="block-tny"><img src="/img/triangle.svg" alt="" ></div>
            <div class="block-tny">ggg</div>
            <div class="block-tny">ggg</div>
            <div class="block-tny">ggg</div>
          </div>
          <div class="block-sm">
            <div class="block-tny"></div>
            <div class="block-tny block-tny--inverted"><h1>HH</h1></div>
            <img class="block-tny" src="/img/circle.svg" alt="" >
            <div class="block-tny"></div>
          </div>
          <img class="block-sm" src="/img/D.png" alt="" >
          <img class="block-sm" src="/img/preview.png" alt="" >
        </div>
    </main>
    <footer>
    </footer>
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
  --main-color: #DBAC79;
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
  padding: 48px 12px;
}

#app {
  font-family: Arial, Helvetica, Arial, sans-serif;
  font-weight: 800;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1, h2, h3, h4, h5, h6 {
  font-family: "Arial Black";
  line-height: 1em;
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

  text-align: center;
  line-height:160px;

  border: 1px solid var(--base-color);
  margin: -1px;
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

</style>
