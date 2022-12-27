<template>
<HeaderComponent v-if="showHeader"/>
<button @click="showHeader = !showHeader">Ativar e desativar</button>
</template>

<script>
  import HeaderComponent from './HeaderComponent.vue';
export default {
  name: 'HelloWorld',
  components:{
    HeaderComponent
  },
  props: {
  },
  data(){
    return{
      showHeader: true,
    }
  }
}
</script>
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
