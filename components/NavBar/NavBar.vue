<template>
  <el-menu
    default-active="0"
    class="el-card is-always-shadow"
    mode="horizontal"
    background-color="var(--gray)"
    text-color="#fff"
    active-text-color="var(--green)"
  >
    <el-menu-item
      v-for="(menuItem, index) in menuItems"
      :key="menuItem.name"
      :index="index"
    >
      <nuxt-link :to="menuItem.path">{{
        menuItem.name
      }}</nuxt-link></el-menu-item
    >
  </el-menu>
</template>
<script>
export default {
  data: () => {
    return {
      menuItems: [
        {
          name: 'Index',
          path: 'Index'
        },
        {
          name: 'Blog',
          path: 'Blog'
        },
        {
          name: 'About the Author',
          path: 'About'
        }
      ]
    }
  }
}
</script>
<style scoped>
.el-menu.el-menu--horizontal {
  border: 0;
}
.el-menu-item a {
  text-decoration: none;
}
</style>
