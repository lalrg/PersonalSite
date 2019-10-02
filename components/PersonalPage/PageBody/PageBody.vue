<template>
  <el-collapse v-model="activeCollapses">
    <el-collapse-item
      v-for="bodySection in bodySections"
      :key="bodySection.name"
      :name="bodySection.name"
    >
      <template slot="title">
        <div class="center-text">
          <i :class="`el-icon-${bodySection.icon}`" />&nbsp;&nbsp;
          <h4>{{ bodySection.name }}</h4>
          &nbsp;&nbsp;
          <i :class="`el-icon-${bodySection.icon}`" />
        </div>
      </template>
      <component :is="`PageBody${bodySection.component}`"></component>
    </el-collapse-item>
  </el-collapse>
</template>
<script>
import PageBodyAbout from '~/components/PersonalPage/PageBody/PageBodyAbout.vue'
import PageBodyTechnologies from '~/components/PersonalPage/PageBody/PageBodyTechnologies.vue'
import PageBodyExperience from '~/components/PersonalPage/PageBody/PageBodyExperience.vue'
export default {
  components: { PageBodyAbout, PageBodyTechnologies, PageBodyExperience },
  data: () => {
    return {
      bodySections: [
        {
          icon: 'user',
          name: 'About me',
          component: 'About',
          active: true
        },
        {
          icon: 'star-off',
          name: 'Technologies',
          component: 'Technologies',
          active: true
        },
        {
          icon: 'suitcase',
          name: 'Working Experience',
          component: 'Experience',
          active: true
        }
      ]
    }
  },
  computed: {
    activeCollapses() {
      const filtered = this.bodySections.filter((item) => {
        return item.active === true
      })

      const activeNames = filtered.map((item) => {
        return item.name
      })

      return activeNames
    }
  }
}
</script>
<style scoped>
h4 {
  display: inline;
}
</style>
