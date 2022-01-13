<template>
  <main>
    <div class="container text-center">
      <h1>{{ title }}</h1>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
  data() {
    return {
      title: 'Lista Prodotti'
    }
  }
}
</script>

<style lang="scss" scoped>
 @import "../assets/scss/partials/_variables.scss";

  main {
    height: 200px;
    background-image: url(../assets/img/fondo-pag-speciali.jpg);
    h1 {
      font-size: 2em;
      color: $headingsColor
    }
  }
</style>
