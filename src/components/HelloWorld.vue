<template>
  <div class="hello">
    <h1>Hermann Caraballo</h1>
    <h3>VueJS Developer</h3>

    <p>13 años de carrera profesional como desarrollador de los cuales 7 años como Frontend Developer, he tenido la oportunidad de realizar labores como Tech Leader y Project Manager.</p>
    <footer>&copy; 2023</footer>
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
body {
  background: none !important;
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
