<template>
  <div>
    <div class="image-1" />
    <div class="image-2">
      <div class="main-content">
        <div class="topic">
          <div class="title">
            We create media installations and we are very cool and epic
          </div>
        </div>
      </div>
    </div>
    <div class="image-3" />
    <div class="main">
      <div class="main-content">
        <div class="topic-1">
          <div class="title">
            Working together with Ebay on this cool campaign for the bees
          </div>
          <div class="content">
            <div class="detail-1">
              We teamed up with the Mediasphere for Nature team to deliver a
              unique augmented reality museum experiment at the Museum für
              Naturkunde Berlin during Lange Nacht der Museen.
            </div>
            <div class="detail-2">
              <div>
                <div class="item">
                  <span class="number">0</span>
                  <span class="text">bees were harmed</span>
                </div>
                <div class="item">
                  <span class="number">2.000.000</span>
                  <span class="text">clicks in one day</span>
                </div>
              </div>
            </div>
          </div>
          <div class="button-container" @click="gotoProjectDetail()">
            <div class="button">
              Read more about the bees project
              <img
                class="arrow-icon"
                src="~/assets/icons/arrow-right-white.svg"
              />
            </div>
          </div>
        </div>
        <div class="image-4">
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-4-1.png') + ')'
              }"
            />
          </div>
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-4-2.png') + ')'
              }"
            />
          </div>
        </div>
        <div class="image-5">
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-5.png') + ')'
              }"
            />
          </div>
        </div>
        <div class="image-6">
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-6-1.png') + ')'
              }"
            />
          </div>
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-6-2.png') + ')'
              }"
            />
          </div>
        </div>
      </div>
      <div class="image-7">
        <div class="image" />
      </div>
      <div class="main-content">
        <div class="topic-1">
          <div class="title">
            Breathing life, soul, and creativity into a space at Futurium,
            Berlin
          </div>
          <div class="content">
            <div class="detail-1">
              Futurium is an ambitious new space in Berlin that combines art
              with technology and design. We were asked to design the experience
              for one of the floors, as an area to encourage creativity.
            </div>
            <div class="detail-2">
              <div>
                <div class="item">
                  <span class="number">681</span>
                  <span class="text">shouting children</span>
                </div>
                <div class="item">
                  <span class="number">3.429</span>
                  <span class="text">worms were made</span>
                </div>
              </div>
            </div>
          </div>
          <div class="button-container">
            <div class="button">
              Read more about the shouting children
              <img
                class="arrow-icon"
                src="~/assets/icons/arrow-right-white.svg"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="image-8">
        <div class="image" />
      </div>
      <div class="main-content">
        <div class="topic-1">
          <div class="title">
            Turning a room into a 360 interactive display for Factory, Berlin
          </div>
          <div class="content">
            <div class="detail-1">
              Futurium is an ambitious new space in Berlin that combines art
              with technology and design. We were asked to design the experience
              for one of the floors, as an area to encourage creativity.
            </div>
            <div class="detail-2">
              <div>
                <div class="item">
                  <span class="number">472</span>
                  <span class="text">bananas were eaten</span>
                </div>
              </div>
            </div>
          </div>
          <div class="button-container">
            <div class="button">
              Read more about the bananas
              <img
                class="arrow-icon"
                src="~/assets/icons/arrow-right-white.svg"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="main-content">
        <div class="image-9">
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-9-1.png') + ')'
              }"
            />
          </div>
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-9-2.png') + ')'
              }"
            />
          </div>
        </div>
        <div class="image-10">
          <div class="image-item">
            <div
              class="image"
              :style="{
                backgroundImage:
                  'url(' + require('@/assets/images/wow/image-10.png') + ')'
              }"
            />
          </div>
        </div>
        <div class="together">
          <Together title="Like what you see? maybe we can work together!" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Together from '~/components/Together'

export default {
  name: 'Wow',
  components: {
    Together
  },
  methods: {
    gotoProjectDetail() {
      this.$router.push({
        path: '/Project/1'
      })
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
  justify-content: center;
  align-items: center;
  text-align: center;
}
.main-content {
  margin: 0 auto;
  max-width: 1600px;
}
.topic {
  .title {
    color: $white;
    @media (max-width: $screen-xs-max) {
      font-size: 48px;
      font-weight: bold;
      line-height: 1.21;
      letter-spacing: normal;
      color: $white;
    }
  }
}
.arrow-icon {
  margin-top: -2px;
  margin-left: 0px;
}
.image-1 {
  width: 100%;
  margin-top: -127px;
  height: 100vh;
  background-blend-mode: soft-light;
  background-image: linear-gradient(
      to bottom,
      rgba(0, 0, 0, 0.7),
      rgba(0, 0, 0, 0.7)
    ),
    url('~@/assets/images/wow/image-1.png');
  background-size: cover;

  @media (max-width: $screen-xs-max) {
    margin-top: -80px;
  }
}
.image-2 {
  background-image: linear-gradient(to bottom, #0b004d, #560065),
    url('~@/assets/images/footer.png');
  background-blend-mode: multiply;
  background-size: cover;
  color: white;
  height: 100vh;
  font-family: 'Bluu Next';

  .topic {
    padding: 0px;
    width: 70%;

    @media (max-width: $screen-xs-max) {
      width: 100%;
      padding: 50px 30px;
    }
  }

  .main-content {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
  }
}
.image-3 {
  background-blend-mode: soft-light;
  background-image: linear-gradient(to bottom, #00000040, #00000040),
    url('~@/assets/images/wow/image-2.png');
  background-size: cover;
  height: 100vh;
  width: 100%;

  @media (max-width: $screen-xs-max) {
    height: 400px;
    background-position: center;
  }
}
.image-4 {
  display: flex;
  padding: 0px 10px;

  @media (max-width: $screen-xs-max) {
    display: block;
    padding: 0px;
  }
}
.image-5 {
  padding: 0px 10px;

  @media (max-width: $screen-xs-max) {
    padding: 0px;
  }
}
.image-6 {
  display: flex;
  padding: 0px 10px;

  @media (max-width: $screen-xs-max) {
    display: block;
    padding: 0px;
  }
}
.image-7 {
  margin-top: 100px;
  .image {
    background-blend-mode: soft-light;
    background-image: linear-gradient(to bottom, #00000040, #00000040),
      url('~@/assets/images/wow/image-7.png');
  }
}
.image-8 {
  margin-top: 100px;
  .image {
    background-blend-mode: soft-light;
    background-image: linear-gradient(to bottom, #00000040, #00000040),
      url('~@/assets/images/wow/image-8.png');
  }
}
.image-9 {
  display: flex;
  padding: 0px 10px;

  @media (max-width: $screen-xs-max) {
    display: block;
    padding: 0px;
  }
}
.image-10 {
  margin-bottom: 150px;
  padding: 0px 10px;

  @media (max-width: $screen-xs-max) {
    padding: 0px;
  }
}
.image-item {
  flex: 1;
  margin: 10px;

  @media (max-width: $screen-xs-max) {
    padding: 10px;
  }
}
.image {
  width: 100%;
  padding-top: 56.25%;
  height: 0px;
  overflow: hidden;
  background-size: cover;
}
.main {
  background-blend-mode: multiply;
  background-image: linear-gradient(to bottom, #34003d, #080039);
  padding: 50px 0px;
}
.topic-1 {
  padding: 100px 150px;
  color: white;

  .title {
    @include desktoptitleh2();
    color: $white;

    @media (max-width: $screen-xs-max) {
      @include mobiletitleh3();
      color: $white;
    }
  }

  .content {
    margin-top: 100px;
    display: flex;
    flex-wrap: wrap;

    .detail-1 {
      @include desktopplarge();
      color: $white;
      flex: 1;

      @media (max-width: $screen-xs-max) {
        @include mobileplarge();
        color: $white;
        flex: initial;
      }
    }

    .detail-2 {
      flex: 1;
      display: flex;
      justify-content: flex-end;

      .item {
        border-bottom: 1px solid white;
        padding: 10px;

        &:first-child {
          border-top: 1px solid white;
        }

        .number {
          @include desktopimpact();
          color: $white;
        }

        .text {
          @include desktoppregular();
          color: $white;
          margin-left: 10px;

          @media (max-width: $screen-xs-max) {
            @include mobilepmedium();
            color: $white;
          }
        }
      }

      @media (max-width: $screen-xs-max) {
        flex: initial;
        margin-top: 50px;
      }
    }

    @media (max-width: $screen-xs-max) {
      margin-top: 50px;
    }
  }
  .button-container {
    display: flex;
    justify-content: flex-end;
    margin-top: 10px;

    .button {
      @include buttonlinkwhite();
      background-image: linear-gradient(to top, #120078, #560065);
      padding: 20px 40px;
      width: 320px;
      cursor: pointer;
      text-transform: uppercase;
    }

    @media (max-width: $screen-xs-max) {
      margin-top: 50px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px;
  }
}
.together {
  margin: 100px 80px;

  @media (max-width: $screen-xs-max) {
    margin: 0px 0px 100px 0px;
  }
}
</style>
