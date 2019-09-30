<template>
  <div class="project-item" @click="itemClick(index)">
    <div :style="{ backgroundImage: `url(${image})` }" class="image" />
    <div class="main">
      <div class="sub-title">{{ subtitle }}</div>
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
    image: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    subtitle: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    }
  },
  methods: {
    itemClick(index) {
      this.$router.push({
        path: '/Project/' + index
      })
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

.project-item {
  color: #262626;
  margin: 30px 20px;
  width: 45%;
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

  .sub-title {
    @include mobilesubtitle();
    text-transform: uppercase;

    @media (max-width: $screen-xs-max) {
      @include mobilesubtitle();
    }
  }

  .title {
    @include desktoptitleh3();
    margin: 10px 0px;

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh3();
    }
  }

  .content {
    @include mobileplarge();

    @media (max-width: $screen-xs-max) {
      @include mobilepmedium();
    }
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
