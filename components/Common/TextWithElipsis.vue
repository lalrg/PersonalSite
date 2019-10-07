<template>
  <p
    :class="{ 'elipsis-text': showElipsis }"
    @click="showElipsis = !showElipsis"
  >
    <slot></slot>
  </p>
</template>

<script>
export default {
  data: () => {
    return {
      showElipsis: true
    }
  }
}
</script>

<style scoped>
.elipsis-text {
  width: 55vw;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
