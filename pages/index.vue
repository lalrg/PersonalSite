<template>
  <div>
    <page-header slot="header"></page-header>
    <br />
    <page-body></page-body>
  </div>
</template>

<script>
import PageHeader from '~/components/PersonalPage/PageHeader/PageHeader.vue'
import PageBody from '~/components/PersonalPage/PageBody/PageBody.vue'

export default {
  components: {
    PageHeader,
    PageBody
  },
  data() {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
    handleSelect(key, keyPath) {}
  }
}
</script>
