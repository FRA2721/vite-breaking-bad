<!-- script-section -->
<script>

// import-axios
import axios from "axios";

// import-AppHeader.vue
import AppHeader from "./components/AppHeader.vue";
export default {
  components: {
    AppHeader,
  }
} 
</script>
<!-- /script-section -->

<!-- template-section -->
<template>
  <AppHeader />
</template>
<!-- /tempalte-section -->

<!-- style-section -->
<style lang="scss">
@use "./styles/general.scss" as *;
</style>
<!-- /style-section -->