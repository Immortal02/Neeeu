<template>
  <div class="vision">
    <div class="container main-content">
      <div class="topic">
        <div class="title">OUR WORK</div>
        <div class="sub-title">
          We believe the best design comes from a deep understanding of people,
          context, and technology.
        </div>
        <div class="detail">
          <div>READ MORE</div>
          <img class="arrow-icon" src="~/assets/icons/arrow-right.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.vision {
  background-image: linear-gradient(
      to bottom,
      rgba(11, 0, 77, 0.7),
      rgba(47, 0, 88, 0.9) 52%,
      rgba(86, 0, 101, 0.7)
    ),
    url('~@/assets/images/home/vision-background.png');
  background-size: cover;
  color: white;
  padding: 150px 0px;
  margin: 100px 0px;
  height: 100vh;
  display: flex;
  align-items: center;

  .main-content {
    margin: 0 auto;
    max-width: 1600px;
  }

  .topic {
    width: 90%;

    .sub-title {
      @media (max-width: 850px) {
        font-size: 33px;
        font-weight: bold;
        line-height: 1.1;
      }
    }

    @media (max-width: 850px) {
      width: 100%;
    }
  }

  .detail {
    font-size: 12px;
    font-weight: bold;
    line-height: 2.08;
    letter-spacing: 3px;
    text-align: right;
    padding: 30px 0px;
    color: white;
    align-items: center;
    display: flex;
    justify-content: flex-end;

    .arrow {
      font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont;
      font-size: 20px;
      color: white;
      padding: 0px 10px;
    }

    @media (max-width: 850px) {
      margin-top: 50px;
    }
  }

  @media (max-width: 850px) {
    padding: 50px 0px;
  }
}
</style>
