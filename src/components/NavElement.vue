<template>
  <li>
    <a
      :class="(classElement == true) ? 'active' : ''"
      :href="hrefElement"
    >{{ text }}</a>
  </li>
</template>

<script>
export default {
  name: 'NavElement',
  props: ['classElement', 'hrefElement', 'text']
}
</script>

<style lang="scss">
</style>