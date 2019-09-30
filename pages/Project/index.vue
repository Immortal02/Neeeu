<template>
  <div class="container main-content">
    <div class="topic">
      <div class="sub-title">OUR WORK</div>
      <div class="title">
        Here you can see our projects
      </div>
    </div>
    <div class="projects">
      <ProjectItem
        v-for="(item, index) in projectData"
        :key="index"
        v-bind="item"
      />
    </div>
    <Together />
  </div>
</template>

<script>
import ProjectItem from '~/components/ProjectItem'
import Together from '~/components/Together'
import ProjectData from '~/assets/projects-data'

export default {
  name: 'Project',
  components: {
    ProjectItem,
    Together
  },
  data() {
    return {
      projectData: ProjectData
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

  @media (max-width: $screen-xs-max) {
    padding: 50px 30px 30px 30px;
  }
}
.projects {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 100px;
}
.together {
  justify-content: space-between;
}
</style>
