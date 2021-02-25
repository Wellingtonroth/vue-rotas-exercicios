<template>
  <div class="usuario-editar">
    <h3>Usuário Editar</h3>
    <p><strong>Código:</strong>{{ id }} ou {{ $route.params.id }}</p>
  </div>
</template>

<script>
export default {
  props: ['id'],
}
</script>

<style>

</style>