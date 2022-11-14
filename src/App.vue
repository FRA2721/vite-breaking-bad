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
  created() {

    this.store.loader = true;
    // axios
    axios

    // get-API
    .get("https://www.breakingbadapi.com/api/characters")

    .then( (resp) => {
      this.store.actors = resp.data;
      console.log(this.store.actors);
      this.store.loader = false;
    })
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
    <AppCardsActorsList />
    <AppLoadingSection  v-if="store.loader" />
  </main>
  <!-- /main -->

</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss">
@use "./styles/general.scss" as *;
</style>
<!-- /style-section -->