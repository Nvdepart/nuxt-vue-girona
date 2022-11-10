<template>
  <v-app>
    <v-main>
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/lista-usuaris">Lista en vue</nuxt-link>
      <nuxt-link to="/usuaris-vue">Usuaris en vue</nuxt-link>
      <nuxt-link to="/contador">Contador</nuxt-link>
      <nuxt-link to="/contador-propi">Contador propi</nuxt-link>
      <nuxt-link to="/functions"> Funcio amb Es6</nuxt-link>
      <nuxt-link to="/porfoli">Porfoli</nuxt-link>
      <nuxt/>
    </v-main>
   </v-app>
</template>

<script>
export default{
  created(){
    console.log("S'ha creat el layout")
  },
  mounted(){
    console.log("S'ha muntat el layout")
  }
}
</script>