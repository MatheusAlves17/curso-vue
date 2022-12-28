<template>
  <HeaderComponent status="success"/>
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
<style scoped>
</style>
