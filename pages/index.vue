<template>
  <div>
    <div class="header">
      <div class="container header-container">
        <div class="header-title">
          This is a very cool and very amazing headline
        </div>
      </div>
    </div>
    <div class="container main main-content">
      <div class="topic">
        <div class="title">OUR WORK</div>
        <div class="sub-title">Featured projects</div>
      </div>
      <div class="featured-projects">
        <ProjectItem
          v-for="(item, index) in projectsData"
          :key="index"
          v-bind="item"
        />
      </div>
      <div class="button-view">
        <div class="button">
          <div>See more projects</div>
          <div class="icon">👀</div>
        </div>
      </div>
    </div>
    <div class="main-content container">
      <div class="topic">
        <div class="title">OUR EXPERTISES</div>
        <div class="sub-title">We’re more than just a pretty face</div>
        <div class="content">
          Our team got the skills to pay the bills! NEEEU is your full service
          innovation solution. Some of our services:
        </div>
      </div>
    </div>
    <div class="main-content">
      <div class="expertise-items">
        <ExpertiseItem
          v-for="(item, index) in expertiseData"
          :key="index"
          v-bind="item"
        />
      </div>
    </div>
    <div class="container main-content">
      <div class="skill">
        <div class="topic">
          <div class="title">OUR SKILLSET</div>
          <div class="sub-title">We’re more than just a pretty face</div>
          <div class="content">
            Our team got the skills to pay the bills! NEEEU is your full service
            innovation solution. Some of our services:
          </div>
        </div>
        <div class="skills">
          <div v-if="$device.isDesktop">
            <img class="jewel-1" src="~/assets/images/home/jewel-1.png" />
            <img class="jewel-2" src="~/assets/images/home/jewel-2.png" />
            <img class="jewel-3" src="~/assets/images/home/jewel-3.png" />
          </div>
          <div v-else>
            <img class="jewel-4" src="~/assets/images/home/jewel-4.png" />
            <img class="jewel-5" src="~/assets/images/home/jewel-5.png" />
            <img class="jewel-6" src="~/assets/images/home/jewel-6.png" />
          </div>
          <div class="skill-row">
            <div class="skill-item">Prototyping</div>
            <div class="skill-item">Workshops</div>
            <div class="skill-item">Design sprints</div>
          </div>
          <div class="skill-row">
            <div class="skill-item">UI/UX</div>
            <div class="skill-item">Prototyping</div>
            <div class="skill-item">Design sprints</div>
            <div class="skill-item">Workshops</div>
          </div>
          <div class="skill-row">
            <div class="skill-item">UI/UX</div>
            <div class="skill-item">Design sprints</div>
            <div class="skill-item">Prototyping</div>
          </div>
        </div>
      </div>
    </div>
    <VisionSlide />
    <div class="container main-content">
      <QuoteSlide />
      <Together />
      <PartnerSlide />
    </div>
  </div>
</template>

<script>
import ProjectItem from '~/components/ProjectItem'
import ExpertiseItem from '~/components/ExpertiseItem'
import Together from '~/components/Together'
import VisionSlide from '~/components/VisionSlide'
import QuoteSlide from '~/components/QuoteSlide'
import PartnerSlide from '~/components/PartnerSlide'
import ProjectsData from '~/assets/projects-data'
import ExpertiseData from '~/assets/expertise-data'

export default {
  name: 'Home',
  components: {
    ProjectItem,
    ExpertiseItem,
    Together,
    VisionSlide,
    QuoteSlide,
    PartnerSlide
  },
  data() {
    return {
      projectsData: ProjectsData,
      expertiseData: ExpertiseData
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/global.scss';

.header {
  background-image: linear-gradient(to bottom, #0b004d, #560065),
    url('~@/assets/images/footer.png');
  background-blend-mode: multiply;
  background-size: cover;
  color: white;
  margin-top: -127px;
  height: 100vh;
  font-family: 'Bluu Next';

  .header-container {
    height: 100%;
    display: flex;
    align-items: center;
    margin: 0 auto;
    max-width: 1600px;
  }

  .header-title {
    font-size: 90px;
    text-align: left;
    font-weight: bold;
    line-height: 1.11;
    width: 100%;

    @media (max-width: 1000px) {
      padding: 200px 30px 150px 30px;
      font-size: 78px;
    }

    @media (max-width: $screen-xs-max) {
      padding: 200px 30px 150px 30px;
      font-size: 66px;
      width: 100%;
    }
  }

  @media (max-width: $screen-xs-max) {
    margin-top: -80px;
  }
}
.main-content {
  margin: 0 auto;
  max-width: 1600px;
}
.main {
  margin: 0 auto;
  padding: 30px 0px;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.featured-projects {
  display: flex;
  flex-wrap: wrap;
}

.expertise-items {
  display: flex;
  justify-content: center;
  margin: 0px 0px;
  color: #262626;

  .content {
    font-size: 20px;
    font-weight: 300;
    margin: 30px 0px;

    @media (max-width: 1170px) {
      font-size: 17px;
    }
  }

  @media (max-width: 1170px) {
    flex-wrap: wrap;
  }
}

.button-view {
  text-align: center;
  cursor: pointer;

  .button {
    color: #fff;
    font-size: 20px;
    font-weight: bold;
    font-family: 'Bluu Next';
    line-height: normal;
    letter-spacing: 0.36px;
    padding: 10px;
    width: 270px;
    text-align: center;
    background-image: linear-gradient(90deg, #67ffce, #a88bff);
    box-shadow: 0 4px 8px 0 rgba(76, 87, 123, 0.28);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 30px auto;

    .icon {
      padding: 7px 0px 0px 10px;
    }

    @media (max-width: $screen-xs-max) {
      font-size: 20px;
      padding: 15px;
      width: 270px;
    }
  }
}
.topic {
  width: 70%;

  @media (max-width: $screen-xs-max) {
    width: 100%;
  }
}
.skill {
  margin: 100px 0px;
  color: #262626;

  .title {
    @media (max-width: $screen-xs-max) {
      font-size: 12px;
    }
  }

  .sub-title {
    font-size: 80px;

    @media (max-width: $screen-xs-max) {
      font-size: 56px;
    }
  }

  .content {
    font-size: 20px;
    font-weight: 300;
    margin: 30px 0px 0px 0px;

    @media (max-width: $screen-xs-max) {
      font-size: 17px;
      line-height: 1.76;
    }
  }
}
.skills {
  margin: 50px 20px;
  font-size: 38px;
  font-family: 'Bluu Next';
  line-height: 1.16;
  letter-spacing: normal;
  color: white;
  padding: 50px 20px;
  background-image: linear-gradient(90deg, #3d0cd1, #ac00e8);
  position: relative;

  .jewel-1 {
    position: absolute;
    bottom: 50px;
    right: 20%;
    z-index: 1;
  }

  .jewel-2 {
    position: absolute;
    top: -30px;
    left: 20%;
    z-index: 1;
  }

  .jewel-3 {
    position: absolute;
    bottom: -50px;
    left: 5%;
    z-index: 1;
  }

  .jewel-4 {
    position: absolute;
    top: -100px;
    right: 0px;
    z-index: -1;
  }

  .jewel-5 {
    position: absolute;
    top: 30%;
    left: -20px;
    z-index: 1;
  }

  .jewel-6 {
    position: absolute;
    bottom: -50px;
    right: -20px;
    z-index: 1;
  }

  .skill-row {
    padding: 10px 0px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

    &:nth-child(1) {
      padding: 0px 0px;

      @media (max-width: $screen-xs-max) {
        padding: 0px 20px;
      }
    }

    &:nth-child(3) {
      padding: 0px 0px;

      @media (max-width: $screen-xs-max) {
        padding: 0px 20px;
      }
    }

    .skill-item {
      padding: 10px 20px;
      z-index: 2;

      @media (max-width: $screen-xs-max) {
        padding: 10px 10px;
      }
    }

    @media (max-width: $screen-xs-max) {
      padding: 0px 20px;
    }
  }

  @media (max-width: $screen-xs-max) {
    font-size: 16px;
    padding: 50px 20px;
  }
}
</style>
