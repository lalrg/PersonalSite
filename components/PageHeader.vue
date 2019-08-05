<template>
  <div class="header-grid">
    <div class="container">
      <div>
        <el-avatar
          class="personal-picture"
          :size="150"
          src="/images/Luis-Richmond-2.jpeg"
        ></el-avatar>
      </div>
      <div class="text">
        <h2>
          Luis Alexander Richmond Guzmán
        </h2>
        <h3>
          Software developer
        </h3>
      </div>
    </div>
    <page-header-skills></page-header-skills>
  </div>
</template>
<script>
import PageHeaderSkills from './../components/PageHeaderSkills.vue'
import 'element-ui/lib/theme-chalk/display.css'
export default {
  components: { PageHeaderSkills }
}
</script>
<style>
.container {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 20px;
  align-content: center;
  align-items: center;
}
.text {
  color: var(--gray);
}
.header-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
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
@media (max-width: 599px) {
  .el-avatar {
    height: 100px !important;
    width: 100px !important;
  }
}
</style>
