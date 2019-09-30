<template>
  <div class="expertise-item">
    <div class="image" :style="background(index, image)">
      <div class="main">
        <div class="title">{{ title }}</div>
        <div class="sub-title">{{ subTitle }}</div>
      </div>
      <div class="detail">
        <div class="detail-btn">
          <span>TELL ME MORE</span>
          <img class="arrow-icon" src="~/assets/icons/arrow-right-white.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    index: {
      type: Number,
      default: 1
    },
    image: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    subTitle: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      background(index, image) {
        if (index === 1)
          return `backgroundImage: linear-gradient(to top, rgba(255, 105, 105, 0.9), rgba(203, 52, 157, 0.7) 51%, rgba(153, 0, 206, 0.9)), url(${image})`
        else if (index === 2)
          return `backgroundImage: linear-gradient(to bottom, rgba(49, 0, 195, 0.8), rgba(133, 22, 255, 0.5) 53%, rgba(201, 45, 255, 0.8)), url(${image})`
        else
          return `backgroundImage: linear-gradient(to bottom, rgba(11, 0, 77, 0.8), rgba(50, 0, 89, 0.5) 51%, rgba(86, 0, 101, 0.8)), url(${image})`
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

.expertise-item {
  color: white;
  margin: 10px 0px;
  cursor: pointer;

  @media (max-width: 1170px) {
    width: calc(100% - 60px);
    padding: 0px;
  }
}

.image {
  padding: 30px 30px;
  text-align: left;
  height: 600px;
  padding-top: 50px;
  background-size: cover;
  position: relative;

  @media (max-width: 1170px) {
    padding: 30px;
    height: 500px;
  }
}

.main {
  padding: 0px;
  text-align: left;
  color: white;

  .title {
    @include desktoptitleh3();
    color: $white;
    margin: 20px 0px;

    @media (max-width: 1170px) {
      @include mobiletitleh3();
      color: $white;
    }
  }

  .sub-title {
    @include desktoppregular();
    color: $white;

    @media (max-width: 1170px) {
      @include mobilepregular();
      color: $white;
    }
  }
}
.detail {
  @include buttonlinkwhite();
  text-align: right;
  border-bottom: solid 1px white;
  padding: 10px 0px;
  position: absolute;
  bottom: 50px;
  width: calc(100% - 60px);
  align-items: center;
  display: flex;
  justify-content: flex-end;

  .detail-btn {
    cursor: pointer;
  }

  @media (max-width: 1170px) {
    width: calc(100% - 60px);
  }
}
</style>
