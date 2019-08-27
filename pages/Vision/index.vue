<template>
  <div class="container">
    <VisionCard />
  </div>
</template>

<script>
import VisionCard from '~/components/VisionCard'

export default {
  name: 'Vision',
  components: {
    VisionCard
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  display: flex;
  padding: 0px 0px;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
