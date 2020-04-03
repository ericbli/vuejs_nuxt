<template>
  <!-- 动态的joke含有连接id等信息 -->
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      <p>{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke", //输出单个Joke及id的相关特性joke,id 以便被其它元件调用
  props: ["joke", "id"]
};
</script>

<style>
.joke {
  padding: 1rem;
  border: 1px dotted #ccc;
  margin: 1rem 0;
}
</style>
