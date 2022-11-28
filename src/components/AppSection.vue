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

    <div class="container">
      <div class="content">
        <AppCard
          v-for="character in characters"
          class="ms-card"
          :info="character"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section {
  background-color: white;
}

.content {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
}

.ms-card {
  background-color: #2e3a46;
  margin: 10px 10px;
  width: calc(100% / 5 - 20px);
}
</style>
