<template>
  <div>
    <h1>在线翻译</h1>
    <h5>简单 / 易容 / 便捷</h5>
    <translate-form></translate-form>
    <translate-output></translate-output>
  </div>
</template>

<script>
import translateForm from './translateForm'
import translateOutput from './translateOutput'

export default {
  data () {
    return {}
  },
  components: {
    translateForm,
    translateOutput
  }
}
</script>
