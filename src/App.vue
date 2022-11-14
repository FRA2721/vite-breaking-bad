<!-- script-section -->
<script>

// import-axios
import axios from "axios";

// import-store-code
import { store } from "./store";

// import-AppHeader.vue, AppCardsActorsList.vue
import AppHeader from "./components/AppHeader.vue";
import AppCardsActorsList from "./components/AppCardsActorsList.vue";

export default {
  components: {
    AppHeader, AppCardsActorsList
  },
  data(){
    return {
      // store-code
      store,
    }
  },
  created() {
    // axios
    axios

    // get-API
    .get("https://www.breakingbadapi.com/api/characters")

    .then( (resp) => {
      this.store.actors = resp.data;
      console.log(this.store.actors);
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
  </main>
  <!-- /main -->

</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss">
@use "./styles/general.scss" as *;
</style>
<!-- /style-section -->