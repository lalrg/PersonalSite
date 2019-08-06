<template>
  <div class="header-grid">
    <page-header-presentation></page-header-presentation>
    <page-header-skills></page-header-skills>
  </div>
</template>

<script>
import PageHeaderSkills from '~/components/PageHeader/PageHeaderSkills.vue'
import PageHeaderPresentation from '~/components/PageHeader/PageHeaderPresentation.vue'
import 'element-ui/lib/theme-chalk/display.css'

export default {
  components: { PageHeaderSkills, PageHeaderPresentation }
}
</script>

<style>
@media (min-width: 900px) {
  .header-grid {
    grid-template-columns: 1fr 1fr;
  }
}
@media (max-width: 899px) {
  .header-grid {
    grid-template-columns: 1fr;
  }
}
</style>
