<template>
  <section class="container">
    <div>
      <text-com/>
      <h1 class="title">
        nuxt_ex
      </h1>
      <h2 class="subtitle">
        nuxt_is_vary_
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
        <p class="nuxt_info">
          this is a big nuxt
        </p>
        <nuxt-link to="/home">首页</nuxt-link>
        <nuxt-link to="/login">注册</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
import TextCom from '~/components/TextCom.vue'

export default {
  components: {
    TextCom
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.nuxt_info{
  font-size: 20px;
  color:red;
}
</style>
