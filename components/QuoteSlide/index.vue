<template>
  <div class="quote">
    <div class="body">
      <div class="title">
        <img class="quote-open" src="~/assets/images/home/quote-open.png" />
        I really liked the speaking. As in when you click on one of the birds,
        it automatically starts playing a voice.
        <img class="quote-close" src="~/assets/images/home/quote-close.png" />
      </div>
      <div class="sub-title">
        - Name, visitor of the Museum Für Naturkunde
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.quote {
  padding: 0px 200px;
  margin: 150px auto;
  font-weight: bold;
  display: flex;
  justify-content: center;

  @media (max-width: 900px) {
    padding: 50px 40px;
  }

  @media (max-width: 900px) {
    padding: 0px 40px;
  }
}
.body {
  max-width: 1000px;
  text-align: left;
}
.title {
  font-size: 48px;
  font-family: 'Bluu Next';
  line-height: 1.21;
  letter-spacing: normal;
  color: #262626;
  min-width: 500px;

  .quote-open {
    position: absolute;
    margin: -50px 0px 0px -70px;
    z-index: -1;

    @media (max-width: 900px) {
      margin: -30px 0px 0px -20px;
      width: 100px;
    }
  }

  .quote-close {
    position: absolute;
    margin: -30px 0px 0px -10px;
    z-index: -1;

    @media (max-width: 900px) {
      margin: -30px 0px 0px -10px;
      width: 100px;
    }
  }

  @media (max-width: 900px) {
    min-width: initial;
    font-size: 30px;
    line-height: 1.4;
    letter-spacing: 0.4px;
  }
}
.sub-title {
  font-size: 18px;
  font-weight: 300;
  line-height: normal;
  letter-spacing: 0.53px;
  color: #57595d;
  padding: 30px 0px;

  @media (max-width: 900px) {
    font-size: 16px;
  }
}
</style>
