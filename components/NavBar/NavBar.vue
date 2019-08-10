<template>
  <el-menu
    default-active="/"
    class="el-card is-always-shadow"
    mode="horizontal"
    background-color="var(--gray)"
    text-color="#fff"
    active-text-color="var(--green)"
  >
    <el-menu-item
      v-for="(menuItem, index) in menuItems"
      :key="index"
      :index="menuItem.path"
      @click="redirect(menuItem.path)"
    >
      {{ menuItem.name }}
    </el-menu-item>
  </el-menu>
</template>
<script>
export default {
  data: () => {
    return {
      menuItems: [
        {
          name: 'Index',
          path: '/'
        },
        {
          name: 'Blog',
          path: '/Blog'
        },
        {
          name: 'About the Author',
          path: '/About'
        }
      ]
    }
  },
  methods: {
    redirect(path) {
      this.$router.push(path)
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
