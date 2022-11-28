<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="logo-title align-items-end d-flex p-3 mb-4">
      <div class="logo col-1">
        <img src="../assets/logo.png" alt="" />
      </div>
      <h2 class="col mx-2">Breaking Bad Api</h2>
    </div>
  </header>
</template>

<style lang="scss" scoped>
img {
  max-width: 90%;
}

.logo-title {
  color: white;
}
</style>
