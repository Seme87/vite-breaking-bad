<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="logo-title d-flex align-items-start p-3">
      <div class="logo col-1 align-self-end">
        <img src="../assets/logo.png" alt="" />
      </div>
      <h2 class="col align-self-end mx-2">Breaking Bad Api</h2>
    </div>
  </header>
</template>

<style lang="scss" scoped>
img {
  max-width: 100%;
}
.logo {
  height: 50px;
}
.logo-title {
  color: white;
}
</style>
