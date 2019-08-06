<template>
  <div>
    <page-header slot="header"></page-header>
    <page-body></page-body>
  </div>
</template>

<script>
import PageHeader from '~/components/PageHeader/PageHeader.vue'
import PageBody from '~/components/PageBody/PageBody.vue'
export default {
  components: {
    PageHeader,
    PageBody
  }
}
</script>
