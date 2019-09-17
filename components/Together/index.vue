<template>
  <div class="together">
    <div class="title">{{ title }}</div>
    <div class="button-view">
      <div class="button">Say hi! 👋</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default:
        'Couldn’t find anything that fts your abilities? Make a spontaneous application!'
    }
  }
}
</script>

<style lang="scss" scoped>
.together {
  background-image: linear-gradient(0deg, #560065, #120078);
  color: white;
  font-family: 'Bluu Next';
  padding: 100px 150px;
  margin: 0px 0px 100px 0px;
  font-weight: bold;
  text-align: left;
  display: flex;
  justify-content: center;
  align-items: center;

  @media (max-width: 1100px) {
    display: block;
    padding: 100px 30px;
    text-align: left;
  }
}
.title {
  font-size: 38px;
  line-height: 1.16;
  letter-spacing: normal;
  color: #fff;
  min-width: 600px;

  @media (max-width: 1100px) {
    font-size: 33px;
    min-width: initial;
  }
}
.button-view {
  text-align: center;
  cursor: pointer;
  margin-left: 80px;

  .button {
    color: #fff;
    display: inline-block;
    font-size: 20px;
    padding: 10px;
    width: 160px;
    text-align: center;
    background-image: linear-gradient(90deg, #67ffce, #a88bff);

    @media (max-width: 1100px) {
      font-size: 16px;
      padding: 15px;
      width: 150px;
      margin-top: 30px;
    }
  }

  @media (max-width: 1100px) {
    text-align: left;
    margin-left: 0px;
  }
}
</style>
