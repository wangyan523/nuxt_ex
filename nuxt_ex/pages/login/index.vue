<template>
  <div class="login_box">
    this is login_page
    <nuxt-link to="/login/one">注册</nuxt-link>
    <regist/>
  </div>
</template>

<script>
import Regist from '~/components/regist.vue'
export default {
  name: 'Login',
  components: {
    Regist
  }
}
</script>

<style lang="less" scoped>

</style>


