<template>
  <div class="translateOutput">
    <h4>你要翻译的文本是： {{translateText}}</h4>
    <h4>翻译好的文本是： {{translatedText}}</h4>
  </div>
</template>

<script>
export default {
  computed: {
    // 从 store 中拿取数据
    translatedText () {
      return this.$store.state.translatedText
    },
    translateText () {
      return this.$store.state.translateText
    }
  }
}
</script>
