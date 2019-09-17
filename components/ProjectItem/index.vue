<template>
  <div class="project-item" @click="itemClick()">
    <div :style="{ backgroundImage: `url(${image})` }" class="image" />
    <div class="main">
      <div class="title">{{ title }}</div>
      <div class="sub-title">{{ subTitle }}</div>
      <div class="content">
        {{ content }}
      </div>
    </div>
    <div class="detail">
      <div>READ MORE</div>
      <img class="arrow-icon" src="~/assets/icons/arrow-right.png" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
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
    },
    content: {
      type: String,
      default: ''
    }
  },
  methods: {
    itemClick() {
      this.$router.push({
        path: '/ProjectDetail'
      })
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.project-item {
  color: #262626;
  padding: 30px 20px;
  width: 50%;
  cursor: pointer;

  @media (max-width: 860px) {
    width: 100%;
    padding: 30px 0px;
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
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    line-height: 2.08;
    letter-spacing: 3px;
  }

  .sub-title {
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
    font-size: 20px;
    font-weight: 300;
    line-height: 1.6;
    letter-spacing: normal;

    @media (max-width: $screen-xs-max) {
      font-size: 18px;
    }
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
