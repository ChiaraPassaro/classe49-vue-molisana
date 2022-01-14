<template>
  <footer>
    <div class="container">
      <div class="col">
        <img
          class="logo"
          src="../assets/img/la-molisana-logo.png"
          alt=""
        >
      </div>
      <ul class="col">
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
      </ul>
      <ul class="col">
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
        <li><a href="">link</a></li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
  footer {
    background-image: url(../assets/img/footer-montagne-bottom.jpg);
    background-repeat: repeat-x;
    background-position: bottom left;
    .container {
      display: flex;
      .col {
        flex-basis: calc(100% / 3);
      }
      .logo {
        width: 60%;
      }
      ul {
        list-style: none;
      }
    }
  }
</style>