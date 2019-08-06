<template>
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
</template>
<script>
export default {}
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
@media (max-width: 599px) {
  .el-avatar {
    height: 100px !important;
    width: 100px !important;
  }
}
</style>
