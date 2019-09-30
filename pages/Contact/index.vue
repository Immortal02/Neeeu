<template>
  <div class="main">
    <div class="container relative">
      <div class="item">
        <div class="title">
          Get in touch
          <span class="hand">👉👈</span>
        </div>
        <div class="sub-title-container">
          <span class="sub-title" @click="sendMail()">
            <span>hello@neeeu.io</span>
            <img
              class="arrow-icon"
              src="~/assets/icons/arrow-right-white.svg"
            />
          </span>
        </div>
        <div class="sub-title-container">
          <span class="sub-title" @click="callPhone()">
            <span>+49 176 96607238</span>
          </span>
        </div>
      </div>
      <div class="item">
        <div class="title address">
          You can always find us here
        </div>
        <div class="pointer" @click="showMap()">
          <div class="content">
            Mittenwalder str. 48
          </div>
          <div class="content">
            10961 Berlin, Germany 🇩🇪
          </div>
        </div>
      </div>
      <div class="item">
        <div class="title">
          Or here
        </div>
        <div class="social-col">
          <a href="https://www.instagram.com" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'instagram']"
              class="social-icons"
            />
          </a>
          <a href="https://twitter.com" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'twitter']"
              class="social-icons"
            />
          </a>
          <a href="https://www.instagram.com" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'facebook-f']"
              class="social-icons"
            />
          </a>
          <a href="https://www.facebook.com" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'linkedin-in']"
              class="social-icons"
            />
          </a>
          <a href="https://medium.com" target="_blank">
            <font-awesome-icon
              :icon="['fab', 'medium-m']"
              class="social-icons"
            />
          </a>
        </div>
      </div>
      <div class="item">
        <div class="title relative">
          Or in spaceee
          <span class="char char-1">e</span>
          <span class="char char-2">e</span>
          <span class="char char-3">e</span>
          <span class="char char-4">e</span>
          <span class="char char-5">e</span>
        </div>
        <span class="star star-1">⭐️</span>
      </div>
      <div class="space-1">
        <span class="star star-2">⭐️</span>
        <span class="star star-3">⭐️</span>
        <span class="star star-4">⭐️</span>
        <span class="star star-4">⭐️</span>
      </div>
      <div class="image-content right">
        <img class="image-1" src="~/assets/images/contact/image-1.png" />
        <span class="star star-5">⭐️</span>
      </div>
      <div class="space-2">
        <span class="star star-6">⭐️</span>
        <span class="star star-7">⭐️</span>
        <span class="star star-8">⭐️</span>
        <span class="char char-6">e</span>
        <span class="satellite satellite-1">🛸</span>
      </div>
      <div class="image-content">
        <img class="image-2" src="~/assets/images/contact/image-2.png" />
        <span class="char char-7">e</span>
        <span class="star star-9">⭐️</span>
      </div>
      <div class="space-3">
        <span class="star star-10">⭐️</span>
        <span class="star star-11">⭐️</span>
        <span class="satellite satellite-2">🛸</span>
        <span class="char char-6">e</span>
      </div>
      <div class="image-content right">
        <img class="image-3" src="~/assets/images/contact/image-3.png" />
      </div>
      <div class="space-4">
        <span class="star star-12">⭐️</span>
        <span class="star star-13">⭐️</span>
        <span class="star star-14">⭐️</span>
        <span class="star star-15">⭐️</span>
        <span class="star star-16">⭐️</span>
        <span class="char char-8">e</span>
      </div>
      <div class="image-content">
        <img class="image-4" src="~/assets/images/contact/image-4.png" />
        <span class="char char-9">e</span>
        <span class="star star-17">⭐️</span>
        <span class="star star-18">⭐️</span>
      </div>
      <div class="space-5">
        <span class="star star-19">⭐️</span>
        <span class="star star-20">⭐️</span>
        <span class="star star-21">⭐️</span>
        <span class="char char-9">e</span>
      </div>
      <div class="image-content right">
        <img class="image-5" src="~/assets/images/contact/image-5.png" />
        <span class="char char-10">e</span>
        <span class="star star-22">⭐️</span>
        <span class="star star-23">⭐️</span>
        <span class="satellite satellite-4">🛸</span>
      </div>
      <div class="image-content">
        <img class="image-6" src="~/assets/images/contact/image-6.png" />
        <span class="char char-11">e</span>
        <span class="star star-24">⭐️</span>
        <span class="star star-25">⭐️</span>
      </div>
      <div class="space-6">
        <span class="star star-24">⭐️</span>
        <span class="star star-30">⭐️</span>
        <span class="star star-26">⭐️</span>
        <span class="star star-27">⭐️</span>
        <span class="star star-28">⭐️</span>
        <span class="star star-29">⭐️</span>
        <span class="char char-12">e</span>
        <span class="char char-13">e</span>
        <span class="satellite satellite-5">🛸</span>
        <span class="satellite satellite-6">🛸</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  components: {},
  methods: {
    sendMail() {
      window.location.href = 'mailto:hello@neeeuio'
    },
    callPhone() {
      window.location.href = 'tel:+4917696607238'
    },
    showMap() {
      window.open(
        'https://www.google.com/maps/dir/?api=1&34.1030032,-118.41046840000001'
      )
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';
@import '~assets/scss/fontstyles.scss';

.container {
  margin: 0 auto;
  padding: 0px 0px;
  justify-content: flex-start;
  align-items: center;
  text-align: left;
  max-width: 1600px;

  @media (max-width: 1000px) {
    width: auto;
  }
}
.main {
  background-image: linear-gradient(to bottom, #0b004d, #560065),
    url('~@/assets/images/footer.png');
  background-blend-mode: multiply;
  background-size: cover;
  background-position: center;
  margin-top: -127px;
  padding: 150px 50px;
  padding-top: 250px;
  min-height: 100vh;

  @media (max-width: $screen-xs-max) {
    padding: 100px 0px;
  }
}
.arrow-icon {
  width: 30px;
  margin-left: 10px;
}
.item {
  padding: 100px 50px;

  &:first-child {
    padding-top: 0px;
  }

  .title {
    @include desktoptitleh2();
    color: $white;
    margin: 30px 0px;

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh2();
      color: $white;
    }
  }
  .hand {
    font-size: 42px;
    line-height: 1.5;
    white-space: pre;
  }
  .sub-title-container {
    margin: 20px 0px;
  }
  .sub-title {
    @include desktoptitleh3();
    color: $white;
    align-items: center;
    white-space: pre;
    cursor: pointer;

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh3();
      color: $white;
    }
  }
  .content {
    @include desktoppmedium();
    color: $white;
    white-space: nowrap;

    @media (max-width: $screen-xs-max) {
      @include desktoppmedium();
      color: $white;
    }
  }
  .address {
    width: 60%;

    @media (max-width: $screen-sm-max) {
      width: 100%;
    }
  }
  .social-col {
    display: flex;
    justify-content: flex-start;
    margin-top: 60px;
    .social-icons {
      color: white;
      font-size: 25px;
    }
    a {
      margin: 0px 20px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 100px 30px;
    width: 100%;
  }
}
.star {
  font-size: 10px;
  position: absolute;
}
.char {
  @include desktoptitleh2();
  color: $white;
  position: absolute;
}
.satellite {
  @include desktoptitleh3();
  color: $white;
  position: absolute;
}
.relative {
  position: relative;
}
.right {
  text-align: right;
}
.space-1 {
  height: 300px;
}
.space-2 {
  height: 450px;
}
.space-3 {
  height: 200px;
}
.space-4 {
  height: 350px;
}
.space-5 {
  height: 300px;
}
.space-6 {
  height: 500px;
}
.star-1 {
  right: 3%;
}
.star-2 {
  left: 20%;
}
.star-3 {
  left: 3%;
  margin-top: 150px;
}
.star-4 {
  right: 30%;
  margin-top: 170px;
}
.star-5 {
  right: 3%;
  margin-top: 80px;
}
.star-6 {
  right: 30%;
  margin-top: 50px;
}
.star-7 {
  left: 30%;
  margin-top: 150px;
}
.star-8 {
  left: 5%;
  margin-top: 400px;
}
.star-9 {
  right: 5%;
}
.star-10 {
  left: 30%;
}
.star-11 {
  right: 30%;
  margin-top: 50px;
}
.star-12 {
  left: 10%;
}
.star-13 {
  right: 30%;
}
.star-14 {
  left: 20%;
  margin-top: 300px;
}
.star-15 {
  right: 30%;
  margin-top: 250px;
}
.star-16 {
  right: 3%;
  margin-top: 200px;
}
.star-17 {
  left: 5%;
  margin-top: 10px;
}
.star-18 {
  left: 50%;
  margin-top: 100px;
}
.star-19 {
  left: 3%;
  margin-top: 50px;
}
.star-20 {
  left: 30%;
  margin-top: 100px;
}
.star-21 {
  right: 10%;
  margin-top: 250px;
}
.star-22 {
  left: 10%;
  margin-top: 80px;
}
.star-23 {
  right: 5%;
  margin-top: 100px;
}
.star-24 {
  left: 25%;
  margin-top: 0px;
}
.star-25 {
  right: 15%;
  margin-top: 50px;
}
.star-26 {
  left: 5%;
  margin-top: 250px;
}
.star-27 {
  right: 30%;
  margin-top: 200px;
}
.star-28 {
  left: 20%;
  margin-top: 400px;
}
.star-29 {
  right: 3%;
  margin-top: 400px;
}
.star-30 {
  right: 3%;
  margin-top: 50px;
}
.char-1 {
  margin-top: 30px;
}
.char-2 {
  margin-top: 80px;
  margin-left: 30px;
}
.char-3 {
  margin-top: 140px;
}
.char-4 {
  left: 30%;
  margin-top: 250px;
}
.char-5 {
  left: 20%;
  margin-top: 400px;
}
.char-6 {
  left: 45%;
  margin-top: 70px;
}
.char-7 {
  right: 30%;
}
.char-8 {
  left: 35%;
  margin-top: 100px;
}
.char-9 {
  right: 20%;
  margin-top: 50px;
}
.char-10 {
  left: 35%;
  margin-top: 0px;
}
.char-11 {
  left: 2%;
  margin-top: 150px;
}
.char-12 {
  left: 30%;
  margin-top: 150px;
}
.char-13 {
  right: 30%;
  margin-top: 450px;
}
.satellite-1 {
  right: 25%;
  margin-top: 250px;
}
.satellite-2 {
  left: 5%;
  margin-top: 150px;
}
.satellite-3 {
  right: 25%;
  margin-top: 250px;
}
.satellite-4 {
  left: 20%;
  margin-top: 150px;
}
.satellite-5 {
  right: 30%;
  margin-top: 0px;
}
.satellite-6 {
  left: 20%;
  margin-top: 300px;
}
.image-1 {
  margin: 30px 0px;
  margin-right: 30%;
}
.image-2 {
  margin: 30px 0px;
  margin-left: 35%;
  width: 100px;
}
.image-3 {
  margin: 30px 0px;
  margin-right: 5%;
}
.image-4 {
  margin: 30px 0px;
  margin-left: 10%;
}
.image-5 {
  margin: 50px 0px;
  margin-right: 20%;
  width: 100px;
}
.image-6 {
  margin: 50px 0px;
  margin-left: 5%;
  width: 50px;
}
.image-content {
  @media (max-width: $screen-xs-max) {
    display: none;
  }
}
</style>
