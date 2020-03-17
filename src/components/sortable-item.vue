<template>
  <li class="list-item"><span @click="console">{{item}}</span></li>
</template>

<script>
import { ElementMixin } from 'vue-slicksort';
export default {
  mixins: [ElementMixin],
  props: ['item'],
  methods: {
    console() {
      new Promise((resolve) => {
        resolve(1)
      }).then((res) => {
        alert(res)
      })
    }
  }
}
</script>

<style>
.list-item {
  padding: 10px 5px;
  border: 1px solid #999;
}
</style>
