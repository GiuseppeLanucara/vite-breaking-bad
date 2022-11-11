<script >
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppLoading from "./components/AppLoading.vue";
import { store } from "./store";
export default {
  components: {
    AppHeader,
    AppMain,
    AppLoading
  },
  data() {
    return {
      store
    }
  },
  created() {
    this.store.loading = true
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data;
      console.log(this.store.characters);
      this.store.loading = false
    })
  },
  methods: {
    getSeries() {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppLoading v-if="store.loading" />
  <AppMain v-else />
</template>

<style lang="scss">
@use "./styles/general.scss" as *
</style>
