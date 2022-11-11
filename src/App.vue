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
    this.getSeries()
  },
  methods: {
    getSeries() {
      console.log("Ciao");
      this.store.loading = true
      let apiUrl = "https://www.breakingbadapi.com/api/characters"
      if (this.store.seriesStatus) {
        apiUrl += "?category=Better+Call+Saul";
      }
      axios.get(apiUrl).then((resp) => {
        this.store.characters = resp.data;
        console.log(resp.data)
        console.log(this.store.characters);
        this.store.loading = false
      })
    }
  }
}
</script>

<template>
  <AppHeader @filterSerie="getSeries()" />
  <AppLoading v-if="store.loading" />
  <AppMain v-else />
</template>

<style lang="scss">
@use "./styles/general.scss" as *
</style>
