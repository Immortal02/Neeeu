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
      <div>READ MORE</div>
      <div class="arrow">→</div>
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

.career-item {
  color: #262626;
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

  @media (max-width: $screen-xs-max) {
    top: 40px;
    left: 180px;
  }
}
.jewel-2 {
  position: absolute;
  top: 100px;
  right: 30%;
  z-index: 1;

  @media (max-width: $screen-xs-max) {
    top: 60px;
    right: 0%;
  }
}
.jewel-3 {
  position: absolute;
  top: 80px;
  left: 80px;
  z-index: 1;

  @media (max-width: $screen-xs-max) {
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
    font-size: 48px;
    font-family: 'Bluu Next';
    font-weight: bold;
    margin: 10px 0px;
    line-height: 1.21;
    letter-spacing: normal;

    @media (max-width: $screen-xs-max) {
      font-size: 33px;
    }
  }

  .content {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.78;
    letter-spacing: normal;

    @media (max-width: $screen-xs-max) {
      font-size: 18px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 0px;
  }
}
.detail {
  font-size: 12px;
  font-weight: bold;
  text-align: right;
  border-bottom: solid 1.2px #262626;
  padding: 10px 0px;
  align-items: center;
  display: flex;
  justify-content: flex-end;
  line-height: 2.08;
  letter-spacing: 3px;
  cursor: pointer;

  .arrow {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont;
    font-size: 20px;
    padding: 0px 10px;
  }
}
</style>
