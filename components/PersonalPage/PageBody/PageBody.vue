<template>
  <el-collapse v-model="activeCollapses">
    <el-collapse-item
      v-for="bodySection in bodySections"
      :key="bodySection.name"
      :name="bodySection.name"
    >
      <template slot="title">
        <div class="center-text">
          <i :class="`el-icon-${bodySection.icon}`" />&nbsp;&nbsp;{{
            bodySection.name
          }}&nbsp;&nbsp;
          <i :class="`el-icon-${bodySection.icon}`" />
        </div>
      </template>
      <component :is="`PageBody${bodySection.component}`"></component>
    </el-collapse-item>
  </el-collapse>
</template>
<script>
export default {
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
          name: 'Achievements',
          component: 'Achievements',
          active: true
        },
        {
          icon: 'suitcase',
          name: 'Working Experience',
          component: 'Experience',
          active: true
        },
        {
          icon: 'coffee-cup',
          name: 'Hobbies ',
          component: 'Hobbies',
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
.el-collapse-item__header {
  display: grid;
  grid-template-columns: 1fr auto;
  align-content: center;
  align-items: center;
}
.center-text {
  text-align: center;
}
</style>
