<template>
  <div class="container main-content">
    <div class="topic">
      <div class="sub-title">Careers</div>
      <div class="title">
        Join our team
      </div>
      <div class="content">
        We’re always looking for people who can help us expand what we have to
        offer and bring variety to our skillset.
      </div>
    </div>
    <div class="careers">
      <CareerItem
        v-for="(item, index) in careerData"
        :key="index"
        v-bind="item"
      />
    </div>
    <Together
      title="Couldn’t find anything that fts your abilities? Make a spontaneous application!"
    />
  </div>
</template>

<script>
import CareerItem from '~/components/CareerItem'
import Together from '~/components/Together'
import CareerData from '~/assets/career-data'

export default {
  name: 'Project',
  components: {
    CareerItem,
    Together
  },
  data() {
    return {
      careerData: CareerData
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

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
  padding: 100px 100px 50px 100px;

  .content {
    width: 60%;

    @media (max-width: 600px) {
      width: 100%;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 30px 30px;
  }
}
.careers {
  display: flex;
  flex-wrap: wrap;
  margin: 0px 20%;
  margin-bottom: 100px;

  @media (max-width: $screen-xs-max) {
    margin: 0px 30px;
    margin-bottom: 50px;
  }
}
</style>
