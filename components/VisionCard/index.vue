<template>
  <div class="vision-card">
    <div class="image" :style="{ backgroundImage: `url(${image})` }">
      <div class="title">{{ title }}</div>
      <div class="sub-title">{{ subTitle }}</div>
    </div>
    <div class="content">
      {{ content }}
    </div>
    <div class="thumbnail">
      <img :src="thumbnailImage" class="thumbnail-image" />
      <div class="title">{{ thumbnailTitle }}</div>
      <div class="sub-title">{{ thumbnailSubTitle }}</div>
      <div class="detail">
        <div>READ MORE<span class="arrow"> →</span></div>
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
  }
}
</script>

<style lang="scss" scoped>
.vision-card {
  color: white;
  margin: 100px 0px;
}
.image {
  padding: 30px 30px;
  text-align: left;
  font-weight: 600;
  height: 550px;
  padding-top: 300px;
  background-size: cover;

  .title {
    font-size: 14px;
    margin: 10px 0px;
  }

  .sub-title {
    font-size: 26px;
  }
}
.content {
  color: #333;
  padding: 30px;
  text-align: left;
}
.thumbnail {
  color: black;
  padding: 0px 30px;
  font-weight: 600;
  text-align: left;

  .thumbnail-image {
    width: 100%;
    object-fit: contain;
  }

  .title {
    font-size: 14px;
    margin: 15px 0px;
  }

  .sub-title {
    font-size: 18px;
  }

  .detail {
    font-size: 14px;
    font-weight: 800;
    text-align: right;
    margin: 20px 0px;
    border-bottom: solid 1px black;
    padding: 10px 0px;

    .arrow {
      padding-left: 10px;
    }
  }
}
</style>
