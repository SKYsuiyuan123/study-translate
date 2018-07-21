<template>
  <div class="translateForm">
    <h5>这是输入</h5>
    <form @submit.prevent="formSubmit">
      <input v-model="translateText" type="text" placeholder="请输入你要翻译的内容">
      <select v-model="language" @change="formSubmit">
        <option value="en">English</option>
        <option value="ru">Russian</option>
        <option value="ko">Korean</option>
        <option value="ja">Janpenese</option>
      </select>
      <input type="submit" value="翻译">
    </form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      translateText: '',
      language: 'en'
    }
  },
  methods: {
    formSubmit () {
      // 将数据存储到 store 中
      this.$store.commit('modifyLanguage', this.language)
      this.$store.commit('addTranslateText', this.translateText)
    }
  }
}
</script>
