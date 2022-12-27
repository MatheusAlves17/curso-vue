<template>
  <HeaderComponent>
    <template v-slot:title>Meus pedidos</template>
    <template v-slot:subtitle>Navegue pelos seu histórico de pedidos</template>
    <template v-slot:paragraph>Todos os pedidos que foram feitos, inclusives aqueles que foram cancelados, está aqui. Basta pesquisar...</template>
  </HeaderComponent>
</template>

<script>
  import HeaderComponent from './HeaderComponent.vue';
  export default {
    name: 'HelloWorld',
    components:{
      HeaderComponent,
    },
    props: {
    },
    data(){
      return{
      }
    }
}
</script>
<style>
</style>
