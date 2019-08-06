<template>
  <el-card class="box-card">
    <nuxt />
  </el-card>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath)
    }
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
