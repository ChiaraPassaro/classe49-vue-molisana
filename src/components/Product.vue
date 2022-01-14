<template>
  <div 
    class="product"
  >
    <img
      :class="color"
      :src="img" 
      :alt="alt"
    >
    <h2>{{ titolo }}</h2>
  </div>
</template>

<script>
export default {  
  name: "Product",
  // props: {
  //   img: {
  //     type: String,
  //     default: 'img.png'
  //   },
  //   alt: {
  //     type: String,
  //   },
  //   titolo: {
  //     type: String,
  //   },
  //   // product: Object
  // }
  props: ['img', 'alt', 'titolo'],
  data() {
    return {
      color: 'blue'
    }
  }
}
</script>

<style lang="scss">
  .product {
      flex-basis: calc((100% / 4) - 0.4em);
      margin: 0.2em;
      padding: 1em;
      background-color: white;
      img {
        width: 100%;
      }
    }
</style>