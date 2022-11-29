<script>

import { store } from "../store.js"
export default {
  name: "AppSelect",
  data() {
    return {
      store
    }
  }
};
</script>

<template>
  <div class="mb-4 px-3 d-flex">
    <select class="ms-form form-select" @change="$emit('search')" v-model="store.statusValue">
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>
  </div>
</template>

<style lang="scss" scoped>
.ms-form {
  font-size: 13px;
  width: 20%;
}
</style>
