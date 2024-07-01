<template lang="">
  <div>{{ name }}</div>
  <h2>v-model 鍵入即得</h2>
  <input type="text" v-model="name" /><br />
  <hr />
  <h2>v-model.trim 去除頭尾空白</h2>
  <input type="text" v-model.trim="name" />
  <hr />
  <h2>v-model.lazy 游標跳出 input 輸入框才會寫入變數</h2>
  <input type="text" v-model.lazy="name" />
  <hr />

  <h2>v-once 防止顯示的變數被更改(不明)</h2>
  <p>{{ name }}</p>
  <p v-once>{{ name }}</p>
  <input type="text" v-model="name" />
  <hr />
  <h2>v-pre 直接印出標籤內的原字</h2>
  <p v-pre>{{ name }}</p>
  <input type="text" v-model.lazy="name" />
  <hr />
  <h2>輸入文字框 Textarea</h2>
  <p>{{ text }}</p>
  <textarea v-model="text"></textarea>
  <hr />
  <h2>下拉式選單 select</h2>
  <p>{{ selectValue }}</p>
  <select v-model="selectValue">
    <option value="">select</option>
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
  </select>
  <hr />
  <h2>下拉式選單 select</h2>
  <p>{{ isCheck }}</p>
  <input type="checkbox" v-model="isCheck" />is check
  <hr />
  <h2>下拉式選單 select</h2>
  {{ checkbox }} <br />
  <input type="checkbox" value="0" v-model="checkbox" /> 0
  <input type="checkbox" value="1" v-model="checkbox" /> 1
  <input type="checkbox" value="2" v-model="checkbox" /> 2
  <input type="checkbox" value="3" v-model="checkbox" /> 3
  <hr />
  <h2>單選 radio</h2>
  {{ radio }} <br />
  <input type="radio" value="0" v-model="radio" /> 0
  <input type="radio" value="1" v-model="radio" /> 1
  <input type="radio" value="2" v-model="radio" /> 2
  <input type="radio" value="3" v-model="radio" /> 3
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      name: "",
      text: "",
      selectValue: "",
      isCheck: false,
      checkbox: [],
      radio: "",
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
