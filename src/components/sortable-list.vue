<template>
  <ul class="list">
    <slot />
  </ul>
</template>

<script>
import { ContainerMixin } from 'vue-slicksort';
export default {
  mixins: [ContainerMixin],
}
</script>
<style>
.list {
  max-height: 400px;
  overflow: auto;
}
</style>
