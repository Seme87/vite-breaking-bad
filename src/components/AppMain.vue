<script>
import AppSection from "./AppSection.vue";
import AppSelect from "./AppSelect.vue";
export default {
  name: "appMain",
  components: {
    AppSection,
    AppSelect,
  },
};
</script>

<template>
  <main class="container">
    <AppSelect />
    <AppSection />
  </main>
</template>

<style lang="scss" scoped></style>
