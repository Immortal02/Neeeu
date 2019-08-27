<template>
  <div class="header">
    <img class="logo" src="~/assets/images/logo.svg" />
    <font-awesome-icon icon="bars" class="bars" />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.header {
  margin: 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.logo {
  height: 50px;
}
.bars {
  font-size: 30px;
}
</style>
