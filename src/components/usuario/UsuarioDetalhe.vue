<template>
  <div class="usuario-detalhe">
    <h3>Usuário Detalhe</h3>
    <p><strong>Código:</strong>{{ id }}</p>
    
    <router-link 
      tag="button" 
      primario 
      :to="{
        name: 'editarUsuario', 
        params: { id },
        query: { 
          completo: true, 
          lingua: 'pt' 
          },
        hash: '#rodape'
      }"
    >
    <!-- Formas de usar o to="" -->
    <!-- :to="`/usuario/${id}/editar`" -->
    <!-- :to="`/usuario/${$route.params.id}/editar`" -->
      Editar
    </router-link>
  </div>
</template>

<script>
export default {
  props: ['id'],
  beforeRouteEnter(to, from, next) {
    // console.log(this.id)
    console.log('dentro do componente detalhe')
    // next(vm => {
    //   console.log(vm.id)
    // })
    const autenticado = true
    autenticado ? next() : next(false)
  }
  // data() {
  //   return {
  //     id: this.$route.params.id
  //   }
  // },
  // watch: {
  //   $route(to, from) {
  //     this.id = to.params.id
  //   }
  // },
}
</script>

<style>

</style>