<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";



export default {
  name: "App",
  props: {
    charactersList: {
      type: Array,
      default: []
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      characters: []
    }
  },
  created() {

    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php")
      .then((response) => {
        console.log(response.data.data.slice(0, 20));

        this.characters = response.data.results;
      }
      )
  }

}

</script>

<template>

  <AppHeader />

  <AppMain :charactersList="characters" />

  <AppFooter :charactersCount="characters.length" />




</template>

<style lang="scss">
@import "./styles/main.scss";
</style>
