<template>
<!-- 整个头部装在一个container里面 -->
  <div class="container">
    <AppHeader2 />
    <nuxt />
  </div>
</template>

<script>
import AppHeader2 from "../components/AppHeader"; //引入头部元件

export default {
  components: {
    //输出头部元件 以便被本页面调用，
    AppHeader2
  }
};
</script>


<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #f4f4f4;
}

a {
  color: #666;
  text-decoration: none;
}

ul {
  list-style: none;
}

.container {
  max-width: 800px;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
  background: #fff;
}
</style>
