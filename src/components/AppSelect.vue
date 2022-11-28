<script>
export default {
  name: "AppSelect",
};
</script>

<template>
  <div class="mb-4 px-3 d-flex">
    <select class="ms-form form-select">
      <option selected>Select Category</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>
  </div>
</template>

<style lang="scss" scoped>
.ms-form {
  font-size: 13px;
  width: 20%;
}
</style>
