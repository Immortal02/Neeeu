<template>
  <div class="footer">
    <div class="content">
      <div class="col">
        <div class="title">TALK TO NEU</div>
        <div class="detail" @click="sendMail()">hello@neeeu.io</div>
        <div class="detail" @click="callPhone()">+49 17696607238</div>
      </div>
      <div class="col">
        <div class="title">FIND NEEU</div>
        <div class="pointer" @click="showMap()">
          <div class="detail">NEEEU Spaces GmbH</div>
          <div class="detail">Mittenwalder str. 48</div>
          <div class="detail">10961 Berlin, German 🇩🇪</div>
        </div>
      </div>
      <div class="col">
        <div class="title">REGULATE NEEEU</div>
        <div class="detail">Privacy Policy</div>
        <div class="detail">Impressum</div>
      </div>
      <div class="col social-col">
        <a href="https://www.instagram.com" target="_blank">
          <font-awesome-icon
            :icon="['fab', 'instagram']"
            class="social-icons"
          />
        </a>
        <a href="https://twitter.com" target="_blank">
          <font-awesome-icon :icon="['fab', 'twitter']" class="social-icons" />
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
          <font-awesome-icon :icon="['fab', 'medium-m']" class="social-icons" />
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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

.footer {
  background-image: linear-gradient(to bottom, #0b004d, #560065),
    url('~@/assets/images/footer.png');
  background-blend-mode: multiply;
  background-size: cover;
  color: white;
  min-height: 300px;
  padding: 50px 100px;
  opacity: 70;

  @media (max-width: 680px) {
    padding: 25px 30px;
  }

  .content {
    max-width: 1600px;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;

    .col {
      margin: 50px 0px;
      min-width: 200px;

      @media (max-width: 1260px) {
        flex-basis: initial;
        flex-grow: initial;
        width: 50%;
      }

      @media (max-width: 680px) {
        flex-basis: 0;
        flex-grow: 1;
        width: 100%;
      }
    }

    .social-col {
      display: flex;
      justify-content: space-between;
      margin-top: 60px;
      max-width: 300px;
      .social-icons {
        color: white;
        font-size: 25px;
      }
    }

    @media (max-width: 1260px) {
      padding: 25px 30px;
    }
  }
}
.title {
  @include mobilesubtitle();
  color: white;
  opacity: 0.7;
  margin: 10px 0px;
}
.detail {
  @include mobilepregular();
  color: #ffffff;
  margin: 5px 0px;
}
</style>
