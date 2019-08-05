<template>
  <div>
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <page-header></page-header>
      </div>
    </el-card>
  </div>
</template>

<script>
import PageHeader from './../components/PageHeader.vue'
export default {
  components: {
    PageHeader
  }
}
</script>

<style>
.box-card {
  display: grid;
}
@media (min-width: 900px) {
  .box-card {
    width: 80%;
    margin-left: 10%;
  }
}
@media (max-width: 899px) {
  .box-card {
    width: 95%;
    margin-left: 2.5%;
  }
}
</style>
