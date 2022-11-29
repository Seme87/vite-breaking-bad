<script>
import axios from "axios";
import {store} from "../store.js";

import AppSection from "./AppSection.vue";
import AppSelect from "./AppSelect.vue";
export default {
  name: "appMain",
  components: {
    AppSection,
    AppSelect,
  },
  data(){
    return {
      store,
    }
  },
  methods: {
    searching(){
      console.log('ricerca')
      axios.get("https://www.breakingbadapi.com/api/characters", {
        params:{
          category:this.store.statusValue,
        },
      })
      .then((resp) => {
      console.log(resp.data);
      this.store.characters = resp.data;
    });
    }
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      console.log(resp.data);
      this.store.characters = resp.data;
    });
  },
};
</script>

<template>
  <main class="container">
    <AppSelect @search="searching" />
    <AppSection />
  </main>
</template>

<style lang="scss" scoped></style>
