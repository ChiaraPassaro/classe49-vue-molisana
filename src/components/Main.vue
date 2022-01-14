<template>
  <main>
    <div class="container text-center">
      <h1>{{ title }}</h1>

      <section>
        <h2>Prodotti più acquistati</h2>
        <div class="products">
          <Product
            v-for="(product, index) in products"
            :key="index"
            :img="product.src"
            :alt="product.titolo"
            :titolo="product.titolo"
          />
        </div>
      </section>
      <section>
        <h2>Prodotti recenti</h2>
        <div class="products">
          <Product
            v-for="(product, index) in productsNew"
            :key="index"
            :img="product.src"
            :alt="product.titolo"
            :titolo="product.titolo"
          />
        </div>
      </section>

      <!-- <Product 
          v-for="(product, index) in products" 
          :key="index"
          :props="product"
        /> -->
      <!-- <div 
          v-for="(product, index) in products" 
          :key="index"
          class="product"
        >
          <img
            :src="product.src" 
            :alt="product.titolo"
          >
          <h2>{{ product.titolo }}</h2>
        </div> -->
    </div>
  </main>
</template>

<script>
import Product from "./Product.vue";

export default {
  name: "Main",
  components: {
    Product,
  },
  data() {
    return {
      title: "Lista Prodotti",
      products: [
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
          titolo: "N.4 Spaghetto Quadrato Bucato",
          tipo: "lunga",
          cottura: 6,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
          titolo: "N.5 Fettuccine",
          tipo: "lunga",
          cottura: 13,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
          titolo: "N.6 Linguine",
          tipo: "lunga",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
          titolo: "N.7 Mezze Linguine",
          tipo: "lunga",
          cottura: 11,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
          titolo: "n.11 Spaghettino Quadrato",
          tipo: "lunga",
          cottura: 9,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
          titolo: "N.38 Mezze maniche",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
          titolo: "N.44 Sedani",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
          titolo: "N.49 Sedanini",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
          titolo: "N.53 Lumachine",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/55-chifferi-rigati.jpg",
          titolo: "N.55 Chifferi rigati",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/58-misto-corto.jpg",
          titolo: "N.58 Misto corto",
          tipo: "corta",
          cottura: 9,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/06/84-ditale-quadrato.jpg",
          titolo: "N.84 Ditale Quadrato",
          tipo: "cortissima",
          cottura: 12,
        },
      ],
      productsNew: [
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
          titolo: "N.4 Spaghetto Quadrato Bucato",
          tipo: "lunga",
          cottura: 6,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
          titolo: "N.5 Fettuccine",
          tipo: "lunga",
          cottura: 13,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/6-linguine.jpg",
          titolo: "N.6 Linguine",
          tipo: "lunga",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/7-mezze-linguine.jpg",
          titolo: "N.7 Mezze Linguine",
          tipo: "lunga",
          cottura: 11,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/04/11-spaghettino-quadrato.jpg",
          titolo: "n.11 Spaghettino Quadrato",
          tipo: "lunga",
          cottura: 9,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/38-mezze-maniche.jpg",
          titolo: "N.38 Mezze maniche",
          tipo: "corta",
          cottura: 12,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/44-sedani.jpg",
          titolo: "N.44 Sedani",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/49-sedani.jpg",
          titolo: "N.49 Sedanini",
          tipo: "corta",
          cottura: 8,
        },
        {
          src: "https://www.lamolisana.it/wp-content/uploads/2021/05/53-lumachine.jpg",
          titolo: "N.53 Lumachine",
          tipo: "corta",
          cottura: 12,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/partials/_variables.scss";

main {
  padding: 2em 0;
  background-image: url(../assets/img/fondo-pag-speciali.jpg);
  h1 {
    margin-bottom: 1em;
    font-size: 2em;
    color: $headingsColor;
  }
  section {
      .products  {
        display: flex;
        flex-wrap: wrap;
      }
  }
}
</style>
