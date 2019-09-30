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
@import '~assets/scss/fontstyles.scss';

.impact {
  background-image: linear-gradient(to right, #e74dcb, #9c2cd0);
  padding: 100px 150px;
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
  @include mobilesubtitle();
  color: $white;
  opacity: 0.7;
  text-transform: uppercase;
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
    @include desktopnumbers();

    @media (max-width: $screen-xs-max) {
      @include mobilenumbers();
    }
  }

  .content {
    @include mobileplarge();
    color: $white;
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
