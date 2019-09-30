<template>
  <div class="vision">
    <div class="container main-content">
      <div class="topic">
        <div class="sub-title">OUR APPROCH</div>
        <div class="title">
          We believe the best design comes from a deep understanding of people,
          context, and technology.
        </div>
        <div class="detail">
          <div class="detail-btn" @click="gotoVisionPage()">
            <span>READ MORE</span>
            <img
              class="arrow-icon"
              src="~/assets/icons/arrow-right-white.svg"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    gotoVisionPage() {
      this.$router.push({
        path: '/Vision'
      })
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

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
      color: $white;
      margin-bottom: 20px;
    }

    .title {
      color: $white;

      @media (max-width: 850px) {
        @include mobiletitleh3();
        color: $white;
      }
    }

    @media (max-width: 850px) {
      width: 100%;
    }
  }

  .detail {
    @include buttonlinkwhite();
    align-items: center;
    display: flex;
    justify-content: flex-end;
    margin-top: 50px;

    .detail-btn {
      cursor: pointer;
    }
  }

  @media (max-width: 850px) {
    padding: 50px 0px;
  }
}
</style>
