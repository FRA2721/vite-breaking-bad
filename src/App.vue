<!-- script-section -->
<script>

// import-axios
import axios from "axios";

// import-store-code
import { store } from "./store";

// import-vue-code-section
import AppHeader from "./components/AppHeader.vue";
import AppCardsActorsList from "./components/AppCardsActorsList.vue";
import AppLoadingSection from "./components/AppLoadingSection.vue";

export default {
  components: {
    AppHeader, AppCardsActorsList, AppLoadingSection
  },
  data(){
    return {
      // store-code
      store,
    }
  },
  methods: {
    getActors(){
      this.store.loader = true;
      const data = {
        ...this.store.serie && { category: this.store.serie }
      }
      axios
        .get("https://www.breakingbadapi.com/api/characters", { data })
        .then( (resp) => {
          this.store.actors = resp.data;
          console.log(resp.data);
        })

        .catch( (error) => {
          console.log(error);
        })

        .finally( () => {
          this.store.loader = false;
        });
    }
  },
  created() {
  }
}   
</script>
<!-- /script-section -->

<!-- template-section -->
<template>

  <!-- header -->
  <header>
    <AppHeader />
  </header>
  <!-- /header -->

  <!-- main -->
  <main>
    <AppLoadingSection  v-if="store.loader" />
    <AppCardsActorsList v-else  @changeSerie="getActors"/>
  </main>
  <!-- /main -->

</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss">
@use "./styles/general.scss" as *;
</style>
<!-- /style-section -->