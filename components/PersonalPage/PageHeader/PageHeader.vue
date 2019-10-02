<template>
  <div class="header-grid">
    <page-header-presentation></page-header-presentation>
  </div>
</template>

<script>
import PageHeaderPresentation from '~/components/PersonalPage/PageHeader/PageHeaderPresentation.vue'

export default {
  components: { PageHeaderPresentation }
}
</script>

<style scoped>
.header-grid {
  display: grid;
  grid-template-columns: 1fr;
  align-content: center;
  align-items: center;
}
</style>
