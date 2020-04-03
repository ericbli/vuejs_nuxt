<template>
  <!-- 查询表单，向父元件发送查询单词 -->
  <form @submit.prevent="onSubmit">
    <input type="text" v-model="text" placeholder="Search Jokes..." />
    <input type="submit" value="Search Jokes" />
  </form>
</template>

<script>
export default {
  name: "SearchJokes", //输出 SearchJokes 以便其它元件调用
  data() {
    return {
      text: ""
    };
  },
  methods: {
    onSubmit() {
      // 向父元件发送信息search-text
      this.$emit("search-text", this.text);
      //查询元件清零
      this.text = "";
    }
  }
};
</script>

<style>
</style>
