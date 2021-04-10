<template>
  <section>
    <div>
      <Logo :width="350"/>
      <h1 class="title">NUXT<span class="green">JS</span></h1>
      <h2 class="subtitle">Starter for CodeSandBox</h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation <IconLink/></a>
        <NLink to="/about" class="button--grey">About</NLink>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'
import IconLink from '~/components/IconLink.vue'

export default {
  components: {
    Logo,
    IconLink
  }
}
</script>

<style scoped>

</style>
