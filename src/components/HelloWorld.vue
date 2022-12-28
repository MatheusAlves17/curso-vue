<template>
  <HeaderComponent v-if="showDialog" @feche="fechando()" status="success"/>
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
        showDialog: true
      }
    },
    methods:{
      fechando(){
        this.showDialog = false
        console.log('fechando...')
      }
    }
}
</script>
<style scoped>
</style>
