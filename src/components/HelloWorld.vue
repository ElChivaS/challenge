<template>
  <div class="hello">
    <img alt="Vue logo" src="../assets/logo.png" width="200">
    <h1>Hermann Caraballo</h1>
    <h3>VueJS Developer</h3>
    <p class="mt-3">13 años de carrera profesional como desarrollador web de los cuales 7 años como Frontend Developer, 
      he tenido la oportunidad de realizar labores como Tech Leader y Project Manager.</p>
    <p>Soy una persona dedicada, constantemente busco aprender, revisar, leer sobre lo más nuevo que va saliendo en tecnología 
    y desarrollo; esto en algunas oportunidades me ha hecho mucho bien en el campo personal como académico y laboral inclusive.</p>
    <p class=" mb-5">Estudié en la Universidad Central de Venezuela, Licienciatura en Computación y completé y aprobé el curso de 
    IBM Advanced Career Education for e-business, además de una serie de cursos y tutoriales on-line (principalmente de Udemy y CodeSchools) 
    que constantemente repaso y procuro actualizar para así mantenerme al día, esto ha logrado darme la experiencia con la que hoy en día cuento.</p>
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
.hello {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: #FFF;
  min-height: 400px;
}
h1 {
  margin-top: 23px;
  align-self: center;
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
img {
  align-self: center;
}
p {
  width: 69%;
  align-self: center;
  font-size: 1.2em;
}
</style>
