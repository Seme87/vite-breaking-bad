<script>

import {store} from "../store.js"

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
      store,
      
    };
  },
  
};
</script>

<template>
  <section class="section py-5 px-5">
    {{store.statusValue}}
    <AppFaund class="banner mb-3" />

    <div class="container">
      <div class="content">
        <AppCard
          v-for="character in store.characters"
          class="ms-card p-2"
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
  margin: 10px 5px;
  width: calc(100% / 5 - 10px);
}
</style>
