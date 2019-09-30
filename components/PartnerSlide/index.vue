<template>
  <div class="partner">
    <div class="topic">
      <div class="sub-title">OUR PARTNERS</div>
      <div class="title">Our sexy partners</div>
    </div>
    <div class="gallery">
      <img
        v-for="(item, index) in partnerData"
        :key="index"
        v-bind="item"
        class="partner-item"
        :src="item.image"
      />
    </div>
  </div>
</template>

<script>
import PartnerData from '~/assets/partner-data'

export default {
  name: 'Partner',
  data() {
    return {
      partnerData: PartnerData
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.partner {
  padding: 0px 0px 100px 0px;
}
.topic {
  margin-bottom: 50px;

  @media (max-width: $screen-xs-max) {
    margin-bottom: 0px;
  }
}
.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 0px 50px;

  .partner-item {
    object-fit: contain;
    max-width: 100%;
    margin: 20px 30px;
    cursor: pointer;

    @media (max-width: $screen-xs-max) {
      margin: 20px 10px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 20px 10px;
  }
}
</style>
