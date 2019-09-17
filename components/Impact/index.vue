<template>
  <div class="impact">
    <div class="label">Impact</div>
    <div class="body">
      <div class="item">
        <div class="title">
          56%
        </div>
        <div class="content">
          of visitors had previous experience with augmented reality.
        </div>
      </div>
      <div class="item">
        <div class="title">
          87%
        </div>
        <div class="content">
          of visitors had previous experience with augmented reality.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.impact {
  background-image: linear-gradient(to right, #e74dcb, #9c2cd0);
  color: white;
  font-family: 'Bluu Next';
  padding: 100px 150px;
  font-weight: bold;
  text-align: left;
  align-items: center;
  margin-bottom: 200px;

  @media (max-width: $screen-xs-max) {
    display: block;
    padding: 100px 50px;
    text-align: left;
  }
}
.label {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 500;
  font-style: normal;
  font-stretch: normal;
  line-height: 2.08;
  letter-spacing: 3px;
  margin-bottom: 30px;
}
.body {
  display: flex;
  flex-wrap: wrap;

  @media (max-width: $screen-xs-max) {
    display: block;
  }
}
.item {
  flex: 1;

  .title {
    font-family: 'Bluu Next';
    font-size: 100px;
    font-weight: bold;
    line-height: 0.8;
    letter-spacing: 1.82px;

    @media (max-width: $screen-xs-max) {
      font-size: 90px;
      font-weight: bold;
      letter-spacing: 1.64px;
    }
  }

  .content {
    font-size: 18px;
    font-weight: 300;
    font-style: normal;
    font-stretch: normal;
    line-height: 30px;
    letter-spacing: 0px;
    margin-top: 30px;
    max-width: 340px;
  }

  &:first-child {
    margin-right: 30px;

    @media (max-width: $screen-sm-max) {
      margin-top: 50px;
      margin-right: 0px;
    }
  }
  &:nth-child(2) {
    margin-left: 30px;

    @media (max-width: $screen-sm-max) {
      margin-left: 0px;
      margin-top: 100px;
    }
  }

  @media (max-width: $screen-sm-max) {
    flex: initial;
  }
}
</style>
