<template>
  <div class="expertise-item">
    <div class="image" :style="background(index, image)">
      <div class="main">
        <div class="title">{{ title }}</div>
        <div class="sub-title">{{ subTitle }}</div>
      </div>
      <div class="detail">
        <div>TELL ME MORE</div>
        <img class="arrow-icon" src="~/assets/icons/arrow-right.png" />
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
  font-weight: 600;
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
    font-size: 48px;
    font-family: 'Bluu Next';
    font-weight: bold;
    line-height: 1.21;
    letter-spacing: normal;
    margin: 20px 0px;

    @media (max-width: 1170px) {
      font-size: 33px;
    }
  }

  .sub-title {
    font-size: 17px;
    font-weight: 300;
    line-height: 1.78;
    letter-spacing: normal;
  }
}
.detail {
  font-size: 12px;
  font-weight: bold;
  line-height: 2.08;
  letter-spacing: 3px;
  text-align: right;
  border-bottom: solid 1px white;
  padding: 10px 0px;
  color: white;
  position: absolute;
  bottom: 50px;
  width: calc(100% - 60px);
  align-items: center;
  display: flex;
  justify-content: flex-end;
  cursor: pointer;

  .arrow {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont;
    font-size: 20px;
    color: white;
    padding: 0px 10px;
  }

  @media (max-width: 1170px) {
    width: calc(100% - 60px);
  }
}
</style>
