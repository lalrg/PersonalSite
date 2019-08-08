<template>
  <div>
    <Navbar></Navbar>
    <el-card class="box-card">
      <nuxt />
    </el-card>
  </div>
</template>
<script>
import Navbar from '~/components/NavBar/NavBar.vue'
export default {
  components: { Navbar }
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
