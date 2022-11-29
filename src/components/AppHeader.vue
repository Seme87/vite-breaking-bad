<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="logo-title align-items-end d-flex p-3 mb-4">
      <div class="logo d-flex align-items:end">
        <img src="../assets/logo.png" alt="" />
      </div>
      <h2 class="mx-2">Breaking Bad Api</h2>
    </div>
  </header>
</template>

<style lang="scss" scoped>
img {
  max-width: 100%;
}

h2 {
  font-size: 40px;
}

.logo {
  height: 70px;
  width: 100px;
}

.logo-title {
  color: white;
}
</style>
