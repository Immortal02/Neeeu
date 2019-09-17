<template>
  <div class="vision-card">
    <div class="image" :style="background(image)">
      <div class="main-content">
        <div class="topic">
          <div class="title">{{ title }}</div>
          <div class="sub-title">{{ subTitle }}</div>
        </div>
      </div>
    </div>
    <div class="description main-content">
      <div class="content">
        {{ content }}
      </div>
      <div class="thumbnail">
        <img :src="thumbnailImage" class="thumbnail-image" />
        <div class="title">{{ thumbnailTitle }}</div>
        <div class="sub-title">{{ thumbnailSubTitle }}</div>
        <div class="detail">
          <div>READ MORE</div>
          <img class="arrow-icon" src="~/assets/icons/arrow-right.png" />
        </div>
      </div>
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
    },
    thumbnailImage: {
      type: String,
      default: ''
    },
    thumbnailTitle: {
      type: String,
      default: ''
    },
    thumbnailSubTitle: {
      type: String,
      default: ''
    }
  },
  data() {
    return {
      background(image) {
        return `backgroundImage: linear-gradient(to top, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0) 50%, rgba(0, 0, 0, 0)), url(${image})`
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.vision-card {
  color: white;
  margin: 0px 0px;
}
.main-content {
  margin: 0 auto;
  max-width: 1600px;
  position: relative;
  width: 100%;
  height: 100%;
}
.image {
  padding: 30px 150px;
  text-align: left;
  height: 100vh;
  padding-top: 300px;
  background-size: cover;
  position: relative;

  .topic {
    position: absolute;
    bottom: 50px;
    padding: 0px;

    .title {
      font-size: 12px;
      font-weight: 500;
    }

    .sub-title {
      font-size: 48px;
      font-weight: bold;

      @media (max-width: $screen-xs-max) {
        font-size: 33px;
      }
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 30px 30px;
  }
}
.description {
  display: flex;
  flex-wrap: wrap;
  padding: 30px 100px;

  @media (max-width: $screen-xs-max) {
    display: block;
    padding: 20px 0px;
  }
}
.content {
  flex: 3;
  color: #262626;
  padding: 30px;
  text-align: left;
  font-size: 20px;
  font-weight: 300;

  @media (max-width: $screen-xs-max) {
    font-size: 18px;
  }
}
.thumbnail {
  flex: 2;
  color: #262626;
  padding: 30px 30px;
  text-align: left;

  .thumbnail-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }

  .title {
    font-size: 14px;
    font-weight: 500;
    margin: 15px 0px;

    @media (max-width: $screen-xs-max) {
      font-size: 12px;
    }
  }

  .sub-title {
    font-size: 22px;
    font-weight: bold;

    @media (max-width: $screen-xs-max) {
      font-size: 20px;
    }
  }

  .detail {
    font-size: 12px;
    font-weight: bold;
    text-align: right;
    margin: 20px 0px;
    border-bottom: solid 1px #262626;
    padding: 10px 0px;
    align-items: center;
    display: flex;
    justify-content: flex-end;
    cursor: pointer;

    .arrow {
      font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont;
      font-size: 20px;
      padding-left: 10px;
    }
  }
}
</style>
