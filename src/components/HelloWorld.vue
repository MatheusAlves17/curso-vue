<template>
  <HeaderComponent
    v-if="showHeader"
  />
  <h1 v-if="accessLevel === 'rh'">Olá, RH!</h1>
  <h1 v-else-if="accessLevel === 'dev'">Olá, Dev!</h1>
  <h1 v-else-if="accessLevel === 'admin'">Olá, Admin!</h1>
  <h1 v-else>Olá, User!</h1>

</template>

<script>
  import HeaderComponent from './HeaderComponent.vue';
export default {
  name: 'HelloWorld',
  components:{
    HeaderComponent
  },
  props: {
    msg: String
  },
  data(){
    return{
      showHeader: true,
      accessLevel: 'rh'
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
