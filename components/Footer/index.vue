<template>
  <div class="footer">
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
      <font-awesome-icon :icon="['fab', 'instagram']" class="social-icons" />
      <font-awesome-icon :icon="['fab', 'twitter']" class="social-icons" />
      <font-awesome-icon :icon="['fab', 'facebook-f']" class="social-icons" />
      <font-awesome-icon :icon="['fab', 'linkedin-in']" class="social-icons" />
      <font-awesome-icon :icon="['fab', 'medium-m']" class="social-icons" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.footer {
  background-image: url('~@/assets/images/footer.png');
  color: white;
  min-height: 300px;
  padding: 25px 30px;

  .col {
    margin: 50px 0px;
  }

  .social-col {
    display: flex;
    justify-content: space-between;
    .social-icons {
      color: white;
      font-size: 25px;
    }
  }
}
.title {
  font-size: 16px;
  color: #c6c3d9;
  margin: 10px 0px;
}
.detail {
  font-size: 16px;
  color: #ffffff;
  margin: 5px 0px;
}
</style>
