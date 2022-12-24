<template>
  <HeaderComponent
    v-if="showHeader"
  />

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
