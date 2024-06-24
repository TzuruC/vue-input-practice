<template lang="">
  <div>{{ name }}</div>
  <label>v-model 鍵入即得 </label>
  <input type="text" v-model="name" /><br />
  <hr />
  <label>v-model.trim 去除頭尾空白 </label>
  <input type="text" v-model.trim="name" />
  <hr />
  <label>v-model.lazy 游標跳出 input 輸入框才會寫入變數 </label>
  <input type="text" v-model.lazy="name" />
  <hr />

  <label>v-once 防止顯示的變數被更改(不明) </label>
  <p v-once>{{ name }}</p>
  <input type="text" v-model="name" />
  <hr />
  <label>v-pre 直接印出標籤內的原字</label>
  <p v-pre>{{ name }}</p>
  <input type="text" v-model.lazy="name" />
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      go: "go",
      name: "",
    };
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
