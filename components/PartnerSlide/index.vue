<template>
  <div class="partner">
    <div class="topic">
      <div class="title">OUR PARTNERS</div>
      <div class="sub-title">Our sexy partners</div>
    </div>
    <div class="gallery">
      <img class="partner-item" src="~/assets/images/home/partner-1.png" />
      <img class="partner-item" src="~/assets/images/home/partner-2.png" />
      <img class="partner-item" src="~/assets/images/home/partner-3.png" />
      <img class="partner-item" src="~/assets/images/home/partner-4.png" />
      <img class="partner-item" src="~/assets/images/home/partner-5.png" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.partner {
  padding: 0px 0px 100px 0px;

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px;
  }
}
.topic {
  margin-bottom: 50px;
}
.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 0px 50px;

  .partner-item {
    object-fit: contain;
    max-width: 100%;
    padding: 20px 30px;
    cursor: pointer;

    @media (max-width: $screen-xs-max) {
      padding: 20px 10px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 20px 10px;
  }
}
</style>
