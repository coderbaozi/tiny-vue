<template>
  <div class="input-wrap">
    <tiny-input v-model="input" type="textarea" counter show-word-limit :maxlength="20"></tiny-input>
  </div>
</template>

<script lang="jsx">
import { Input } from '@opentiny/vue'

export default {
  components: {
    TinyInput: Input
  },
  data() {
    return {
      input: '测试 counter 属性'
    }
  }
}
</script>

<style>
.input-wrap {
  padding-top: 20px;
  height: 100%;
  background: #f4f4f4;
}
</style>
