<script>
import axios from "axios";
import AppFaund from "./AppFaund.vue";
import AppCard from "./AppCard.vue";
export default {
  name: "AppSection",
  components: {
    AppFaund,
    AppCard,
  },
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      console.log(resp.data);
      this.characters = resp.data;
    });
  },
};
</script>

<template>
  <section class="section py-5 px-5">
    <AppFaund class="banner mb-3" />
    <div class="row row-cols-5 justify-content-center px-2 py-3 g-3 gx-3">
      <AppCard
        v-for="character in characters"
        class="col p-2 ms-card"
        :info="character"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section {
  background-color: white;
}

.ms-card {
  background-color: #2e3a46;
}
</style>
