<template>
  <HeaderComponent>
    <template v-slot:description>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Rem reiciendis delectus, unde quidem debitis accusantium? Voluptatibus eum omnis non est eaque? Voluptates dolorum excepturi dicta voluptatem numquam accusamus porro eveniet!
    </template>
  </HeaderComponent>
  <div class="card">
    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Reprehenderit recusandae, sint voluptatem, id similique quidem dignissimos tempore aperiam pariatur molestias consequuntur nemo suscipit sed. Quia impedit provident iusto consequuntur quo?
  </div>
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
  .card{
    padding: 4rem;
    background: #f8f8f8;
    color: cornflowerblue;
    font-weight: 600;
    border-radius: 12px;
    max-width: 400px;
  }
</style>
