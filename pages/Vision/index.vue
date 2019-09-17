<template>
  <div>
    <div class="container main-content">
      <div class="topic">
        <div class="title">OUR VISION</div>
        <div class="sub-title">
          Discover our vision and get the see how epic we are!
        </div>
      </div>
    </div>
    <div>
      <VisionCard
        v-for="(card, index) in visionData"
        :key="index"
        v-bind="card"
      />
    </div>
    <div class="container main-content">
      <Together />
    </div>
  </div>
</template>

<script>
import VisionCard from '~/components/VisionCard'
import Together from '~/components/Together'
import VisionData from '~/assets/vision-data'

export default {
  name: 'Vision',
  components: {
    VisionCard,
    Together
  },
  data() {
    return {
      visionData: VisionData
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.container {
  margin: 0 auto;
  padding: 0px 0px;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.main-content {
  margin: 0 auto;
  max-width: 1600px;
}
.topic {
  padding: 100px 100px 50px 100px;

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px 30px 30px;
  }
}
</style>
