<template>
  <div class="hello">
    <img alt="sjf logo" src="../assets/head.jpg">
    <h1>{{ msg }}</h1>
    <p>Web Developer from Minneapolis. Enjoying the never ending learning and new things to do in the world of web dev.</p>
    <ul>
      <li><a href="mailto:sam.j.fortin@gmail.com" target="_blank" rel="noopener">gmail</a></li>
      <li><a href="https://github.com/sjfortin" target="_blank" rel="noopener">github</a></li>
      <li><a href="https://www.linkedin.com/in/samfortin/" target="_blank" rel="noopener">linkedin</a></li>
      <li><a href="https://codepen.io/sjfortin/" target="_blank" rel="noopener">codepen</a></li>
      <li><a href="https://sjfortin.com" target="_blank" rel="noopener">portfolio of some work</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  border-radius: 50%;
  width: 140px;
  height: 140px;
}
h1 {
  margin-top: 0;  
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
