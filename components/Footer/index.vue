<template>
  <div class="footer">
    <div class="content">
      <div class="col">
        <div class="title">TALK TO NEU</div>
        <div class="detail">hello@neeeu.io</div>
        <div class="detail">+49 17696607238</div>
      </div>
      <div class="col">
        <div class="title">FIND NEEU</div>
        <div class="detail">NEEEU Spaces GmbH</div>
        <div class="detail">Mittenwalder str. 48</div>
        <div class="detail">10961 Berlin, German 🇩🇪</div>
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
export default {}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.footer {
  background-image: linear-gradient(to bottom, #0b004d, #560065),
    url('~@/assets/images/footer.png');
  background-blend-mode: multiply;
  background-size: cover;
  color: white;
  min-height: 300px;
  padding: 50px 100px;
  opacity: 70;

  @media (max-width: $screen-xs-max) {
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
    }

    .social-col {
      display: flex;
      justify-content: space-between;
      margin-top: 60px;
      .social-icons {
        color: white;
        font-size: 25px;
      }
    }
  }
}
.title {
  font-size: 12px;
  font-weight: 500;
  font-style: normal;
  font-stretch: normal;
  line-height: 2.08;
  letter-spacing: 3px;
  color: white;
  opacity: 0.7;
  margin: 10px 0px;
}
.detail {
  font-size: 17px;
  font-weight: 300;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.76;
  letter-spacing: normal;
  color: #ffffff;
  margin: 5px 0px;
}
</style>
