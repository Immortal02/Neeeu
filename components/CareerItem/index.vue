<template>
  <div class="career-item" @click="itemClick()">
    <img
      v-if="index === 1"
      class="jewel-1"
      src="~/assets/images/home/jewel-1.png"
    />
    <img
      v-if="index === 2"
      class="jewel-2"
      src="~/assets/images/home/jewel-2.png"
    />
    <img
      v-if="index === 3"
      class="jewel-3"
      src="~/assets/images/home/jewel-3.png"
    />
    <div class="main">
      <div class="title">{{ title }}</div>
      <div class="content">
        {{ content }}
      </div>
    </div>
    <div class="detail">
      <div class="detail-btn">
        <span>READ MORE</span>
        <img class="arrow-icon" src="~/assets/icons/arrow-right-black.svg" />
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
    title: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    }
  },
  methods: {
    itemClick() {
      // this.$router.push({
      //   path: '/'
      // })
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

.career-item {
  padding: 30px 20px;
  width: 100%;
  position: relative;

  @media (max-width: 860px) {
    width: 100%;
    padding: 40px 0px;
  }
}
.jewel-1 {
  position: absolute;
  top: 50px;
  left: 315px;
  z-index: 1;

  @media (max-width: 600px) {
    top: 40px;
    left: 180px;
  }
}
.jewel-2 {
  position: absolute;
  top: 100px;
  right: 30%;
  z-index: 1;

  @media (max-width: 600px) {
    top: 60px;
    right: 0%;
  }
}
.jewel-3 {
  position: absolute;
  top: 80px;
  left: 80px;
  z-index: 1;

  @media (max-width: 600px) {
    top: 10px;
    left: 80px;
  }
}
.image {
  padding-top: 56.25%;
  height: 0px;
  overflow: hidden;
  background-size: cover;
}

.main {
  padding: 20px;
  text-align: left;

  .title {
    @include desktoptitleh3();
    margin: 10px 0px;

    @media (max-width: 600px) {
      @include mobiletitleh3();
    }
  }

  .content {
    @include desktoppregular();

    @media (max-width: 600px) {
      @include mobilepregular();
    }
  }

  @media (max-width: 600px) {
    padding: 0px;
  }
}
.detail {
  @include buttonlinkblack();
  text-align: right;
  border-bottom: solid 1.2px #262626;
  padding: 10px 0px;
  align-items: center;
  display: flex;
  justify-content: flex-end;

  .detail-btn {
    cursor: pointer;
  }
}
</style>
