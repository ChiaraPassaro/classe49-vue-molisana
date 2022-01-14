<template>
  <header>
    <div class="container text-center">
      <img
        src="../assets/img/la-molisana-logo.png"
        alt=""
      >
      <ul class="nav">
        <NavElement 
          v-for="(link, index) in links"
          :key="index"
          :class-element="link.current"
          :href-element="link.url"
          :text="link.text"
          class="nav-element"
        />
        <!-- <li
          v-for="(link, index) in links"
          :key="index"
          @click="changeActive(index)"
        >
          <a
            :class="(link.current == true) ? 'active' : ''"
            :href="link.url"
          >{{ link.text }}</a>
        </li> -->
        <!-- <li>
            <a href="">Home</a>
          </li>
          <li>
            <a href="" class="active">Prodotti</a>
          </li>
          <li>
            <a href="">Chi Siamo</a>
          </li>
          <li>
            <a href="">Contatti</a>
          </li> -->
      </ul>
    </div>    
  </header>
</template>

<script>
import NavElement from "./NavElement.vue";
// import Product from "./Product.vue";


export default {
  name: 'Header',
  components: {
    NavElement
  },
  data() { //data e' una funzione che restituisce il nostro object
    return {
      title: "Lorem Ipsum pippo",
      links: [
                {
                    text: "Home",
                    url: "#",
                    current: false,
                },
                {
                    text: "Prodotti",
                    url: "#",
                    current: true,
                },
                {
                    text: "Chi Siamo",
                    url: "#",
                    current: false,
                },
                {
                    text: "Contatti",
                    url: "#",
                    current: false,
                },
                 {
                    text: "Dove siamo",
                    url: "#",
                    current: false,
                },
            ],
    }
  }, 
  created () {
    console.log('created');
  },
  methods: {
    changeActive(indexElement) {
       this.links.forEach(
        (element, index) => {
          if (index === indexElement) {
            element.current = true;
          } else {
            element.current = false;
          }
        }
      )
    }
  }
}


</script>

<style lang="scss">
  // @import "../assets/scss/partials/_mixins.scss";
  // @import "../assets/scss/partials/_header.scss";
</style>