<script >
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
export default {
  components: {
    AppHeader,
    AppMain
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      console.log(resp);
    })
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use "./styles/general.scss" as *
</style>
