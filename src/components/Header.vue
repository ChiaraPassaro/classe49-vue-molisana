<template>
  <header>
    <div class="container text-center">
      <img src="../assets/img/la-molisana-logo.png" alt="">
        <ul>
          <li @click="changeActive(index)" v-for="(link, index) in links" :key="index" >
           <a :class="(link.current == true) ? 'active' : ''" :href="link.url">{{ link.text }}</a>
          </li>
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
export default {
  name: 'Header',
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

<style lang="scss" scoped>
  ul {
    list-style: none;
    display: flex;
    justify-content: center;
    align-items: center;
    li a {
      display: block;
      text-decoration: none;
      padding: 1em;
      transition: all 0.6s;
      &:hover,
      &:active,
      &.active {
        background-color: aqua;
      }
    }
  }
</style>