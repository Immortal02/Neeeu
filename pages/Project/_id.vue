<template>
  <div>
    <div class="container main-content">
      <div class="topic">
        <div class="sub-title">Museum für Naturkunde</div>
        <div class="title">
          Augmented burdies
        </div>
        <div class="content">
          Augmented reality, sound and birds to bring the collection and
          audience together
        </div>
      </div>
    </div>
    <div class="image-container">
      <img class="image" src="~/assets/images/project-detail/image-1.png" />
    </div>
    <div class="container main-content">
      <div class="topic detail">
        <div class="content">
          We teamed up with the Mediasphere for Nature team to deliver a unique
          augmented reality museum experiment at the Museum für Naturkunde
          Berlin during Lange Nacht der Museen.
        </div>
      </div>
    </div>
    <div class="image-container">
      <img class="image" src="~/assets/images/project-detail/image-2.png" />
    </div>
    <div class="container main-content">
      <div class="topic-1">
        <div class="title-1">
          This is a short text about the challenge of the project
        </div>
        <div class="content-1">
          If today’s museum visitor expects to learn while also having fun at
          the same time, what role, if any, can Augmented Reality have in
          providing this experience? We tried to find out, with a focus on
          surprise, play & education.
        </div>
      </div>
      <div class="bird">
        <img src="~/assets/images/project-detail/bird.png" />
      </div>
      <div class="topic-1">
        <div class="title-1">
          This is a short text about the challenge of the project
        </div>
        <div class="content-1">
          If today’s museum visitor expects to learn while also having fun at
          the same time, what role, if any, can Augmented Reality have in
          providing this experience? We tried to find out, with a focus on
          surprise, play & education.
        </div>
      </div>
      <img src="~/assets/images/project-detail/image-5.png" class="img" />
      <QuoteSlide />
      <Impact />
      <Together />
    </div>
    <div class="container main-content">
      <div class="project-title">
        Related projects
      </div>
      <div class="projects">
        <ProjectItem
          v-for="(item, index) in projectData"
          :key="index"
          v-bind="item"
        />
      </div>
    </div>
    <div class="button-view">
      <div class="button">
        <div>Show other projects</div>
        <div class="icon">👆</div>
      </div>
    </div>
  </div>
</template>

<script>
import ProjectItem from '~/components/ProjectItem'
import Together from '~/components/Together'
import Impact from '~/components/Impact'
import QuoteSlide from '~/components/QuoteSlide'
import ProjectData from '~/assets/projects-data'

export default {
  name: 'Project',
  components: {
    ProjectItem,
    Together,
    QuoteSlide,
    Impact
  },
  data() {
    return {
      projectData: ProjectData.slice(0, 2)
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
.detail.topic {
  margin: 150px 0px;
  padding: 0px 100px;

  .content {
    width: 100%;
  }

  @media (max-width: $screen-xs-max) {
    margin: 100px 0px;
    padding: 0px 30px;
  }
}
.image-container {
  max-width: 1600px;
  margin: auto;

  .image {
    width: 100%;
  }
}
.topic {
  padding: 100px 100px 50px 100px;

  .content {
    @include desktopplarge();
    width: 60%;

    @media (max-width: $screen-sm-max) {
      @include mobileplarge();
      width: 100%;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px 30px 30px;
  }
}
.topic-1 {
  padding: 50px 30px;
  margin: 100px auto;
  text-align: left;
  max-width: 920px;

  .title-1 {
    @include desktopstitle();

    @media (max-width: $screen-xs-max) {
      @include mobilestitle();
    }
  }

  .content-1 {
    @include desktopplarge();
    margin-top: 50px;

    @media (max-width: $screen-xs-max) {
      @include mobilepregular();
      margin-top: 20px;
    }
  }

  @media (max-width: $screen-xs-max) {
    padding: 0px 30px;
    margin: 100px 0px;
  }
}
.bird {
  text-align: center;

  img {
    width: 300px;

    @media (max-width: $screen-xs-max) {
      width: 200px;
    }
  }

  @media (max-width: $screen-xs-max) {
    text-align: center;
    margin: auto;
  }
}
.img {
  width: 100%;
}
.projects {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 30px;
}
.button-view {
  text-align: center;
  margin-bottom: 150px;

  .button {
    @include buttonmain();
    padding: 10px;
    width: 270px;
    text-align: center;
    background-image: linear-gradient(90deg, #67ffce, #a88bff);
    box-shadow: 0 4px 8px 0 rgba(76, 87, 123, 0.28);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 30px auto;
    cursor: pointer;

    .icon {
      padding: 7px 0px 0px 10px;
    }

    @media (max-width: $screen-xs-max) {
      padding: 15px;
      width: 270px;
    }
  }
}
.quote {
  text-align: left;
}
.project-title {
  @include desktoptitleh2();
  text-align: left;
  padding: 100px 0px 0px 20px;

  @media (max-width: $screen-xs-max) {
    @include mobiletitleh2();
  }
}
</style>
