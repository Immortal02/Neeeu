<template>
  <div class="team-member">
    <div class="image" :style="background(image)" />
    <div class="main">
      <div class="title">{{ title }}</div>
    </div>
    <div v-if="level" class="level">{{ level }}</div>
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
    level: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      background(image) {
        return `backgroundImage: url(${image})`
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

.team-member {
  color: white;
  margin: 30px 0px;
  width: 30%;
  height: auto;
  padding-bottom: 30px;
  position: relative;

  @media (max-width: $screen-xs-max) {
    width: calc(50% - 20px);
    margin: 20px 10px;
  }
}

.image {
  padding: 30px 30px;
  text-align: left;
  padding-top: 125%;
  background-size: cover;
  position: relative;

  @media (max-width: 1000px) {
    padding: 30px 10px;
    padding-top: 100%;
  }

  @media (max-width: $screen-xs-max) {
    padding: 30px;
    height: 200px;
  }
}

.main {
  padding: 0px;
  text-align: left;
  color: #262626;

  .title {
    @include desktoptitleh5();
    margin: 10px 0px;

    @media (max-width: 1080px) {
      font-size: 29px;
    }

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh5();
    }
  }
}
.level {
  @include desktoptag();
  width: 100%;
  padding-bottom: 10px;
  text-align: left;
  bottom: 0px;
  border-bottom: solid 1px #262626;

  @media (max-width: $screen-xs-max) {
    @include mobiletag();
  }
}
</style>
