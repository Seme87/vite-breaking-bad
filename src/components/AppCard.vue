<script>
export default {
  name: "Appcard",
  props: {
    info: Object,
  },
};
</script>

<template>
  <div class="text-center">
    <img class="img-fluid" :src="info.img" alt="name" />
    <h3 class="mb-4 mt-2">{{ info.name }}</h3>
    <div class="category">{{ info.category }}</div>
    <div class="status">{{ info.status }}</div>
  </div>
</template>

<style lang="scss" scoped>
h3 {
  color: white;
}
.category,
.status {
  color: #484c53;
}
</style>
