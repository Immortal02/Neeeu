<template>
  <div class="vision-card">
    <div class="image" :style="background(image)">
      <div class="main-content">
        <div class="topic">
          <div class="sub-title">{{ title }}</div>
          <div class="title">{{ subTitle }}</div>
        </div>
      </div>
    </div>
    <div class="description main-content">
      <div class="content">
        {{ content }}
      </div>
      <div class="thumbnail">
        <img :src="thumbnailImage" class="thumbnail-image" />
        <div class="sub-title">{{ thumbnailSubTitle }}</div>
        <div class="title">{{ thumbnailTitle }}</div>
        <div class="detail">
          <div class="detail-btn" @click="itemClick(projectIndex)">
            <span>READ MORE</span>
            <img
              class="arrow-icon"
              src="~/assets/icons/arrow-right-black.svg"
            />
          </div>
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
    projectIndex: {
      type: Number,
      default: 1
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

    .sub-title {
      @include mobilesubtitle();
      color: $white;
    }

    .title {
      @include desktoptitleh3();
      color: $white;

      @media (max-width: 520px) {
        @include mobiletitleh3();
        color: $white;
      }
    }
  }

  @media (max-width: 830px) {
    padding: 30px 30px;
  }
}
.description {
  display: flex;
  flex-wrap: wrap;
  padding: 30px 100px;

  @media (max-width: 1100px) {
    flex-direction: column;
    align-items: center;
    padding: 30px 30px;
  }

  @media (max-width: 520px) {
    flex-direction: column;
    align-items: center;
    display: block;
    padding: 20px 0px;
  }
}
.content {
  @include mobileplarge();
  flex: 3;
  padding: 30px;
  text-align: left;

  @media (max-width: 1100px) {
    width: 500px;
  }

  @media (max-width: 520px) {
    @include mobilepmedium();
    width: auto;
  }
}
.thumbnail {
  flex: 2;
  padding: 30px 30px;
  text-align: left;

  .thumbnail-image {
    width: 100%;
  }

  .sub-title {
    @include desktopsubtitle();
    margin: 15px 0px;

    @media (max-width: 520px) {
      @include mobilesubtitle();
    }
  }

  .title {
    @include desktoptitleh6();

    @media (max-width: 520px) {
      @include mobiletitleh6();
    }
  }

  .detail {
    @include buttonlinkblack();
    text-align: right;
    margin: 20px 0px;
    border-bottom: solid 1px #262626;
    padding: 10px 0px;
    align-items: center;
    display: flex;
    justify-content: flex-end;

    .detail-btn {
      cursor: pointer;
    }
  }

  @media (max-width: 1100px) {
    width: 500px;
  }

  @media (max-width: 520px) {
    width: auto;
  }
}
</style>
