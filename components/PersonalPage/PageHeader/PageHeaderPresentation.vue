<template>
  <div>
    <div class="container">
      <el-avatar
        class="personal-picture"
        :size="150"
        src="/images/Luis-Richmond-2.jpeg"
      ></el-avatar>
      <div class="text">
        <h2>
          Luis Alexander Richmond Guzmán
        </h2>
        <h3>
          Software developer
        </h3>
        <user-social-buttons></user-social-buttons>
      </div>
    </div>
  </div>
</template>
<script>
import UserSocialButtons from '~/components/Common/SocialButtons/UserSocialButtons.vue'
export default {
  components: { UserSocialButtons }
}
</script>
<style scoped>
.container {
  display: grid;
  grid-template-columns: auto 1fr;
  grid-column-gap: 20px;
  align-content: center;
  align-items: center;
}
h3 {
  margin-bottom: 5px;
}
@media (max-width: 599px) {
  .el-avatar {
    height: 100px !important;
    width: 100px !important;
  }
}
</style>
