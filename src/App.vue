<template>
  <div id="app">
    <div class="section">
      <div class="container">
        <div class="box">
          <div class="columns">
            <div class="column is-4">
              <div class="columns is-multiline">
                <div class="column is-2" v-for="(color,index) in colors" v-bind:key="index">
                  <ColorBox v-bind:color="color" @changeColor="setColor" />
                </div>
              </div>
            </div>
            <div
              class="column is-6 is-offset-2 has-text-white"
              v-bind:style="{'background-color': boxColor}"
            >
              <h1 class="title is-1 has-text-white">Vue.js</h1>
              <p
                class="subtitle is-6 para has-text-white"
              >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce semper est sed nunc lobortis, at mollis felis tincidunt. In interdum magna eu egestas euismod. Pellentesque consectetur nunc eget erat elementum, non vehicula dolor egestas. Interdum et malesuada fames ac ante ipsum primis in faucibus.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ColorBox from "./components/ColorBox";
export default {
  name: "App",
  components: {
    ColorBox
  },
  data() {
    return {
      boxColor: "#000",
      colors: [
        "#264653",
        "#2a9d8f",
        "#e9c46a",
        "#f4a261",
        "#e76f51",
        "#ffbe0b",
        "#fb5607",
        "#ff006e",
        "#8338ec",
        "#3a86ff",
        "#f94144",
        "#f3722c",
        "#f8961e",
        "#90be6d",
        "#43aa8b",
        "#577590",
        "#02c39a",
        "#028090"
      ]
    };
  },
  methods: {
    setColor(color) {
      this.boxColor = color;
    }
  }
};
</script>

<style>
body {
  font-family: "Roboto";
}
.para {
  line-height: 180%;
}
</style>
