<template>
  <div class="container">
    <div class="topic">
      <div class="title">OUR VISION</div>
      <div class="sub-title">
        Discover our vision and get the see how epic we are!
      </div>
    </div>
    <div>
      <VisionCard
        v-for="(card, index) in visionData"
        :key="index"
        v-bind="card"
      />
    </div>
  </div>
</template>

<script>
import VisionCard from '~/components/VisionCard'
import VisionData from '~/assets/vision-data'

export default {
  name: 'Vision',
  components: {
    VisionCard
  },
  data() {
    return {
      visionData: VisionData
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  margin: 0 auto;
  padding: 0px 0px;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.topic {
  padding: 50px 30px;
  padding-bottom: 0px;
  text-align: left;
  font-weight: 600;

  .title {
    font-size: 14px;
    margin-bottom: 10px;
  }

  .sub-title {
    font-size: 36px;
  }
}
</style>
