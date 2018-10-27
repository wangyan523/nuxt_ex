<template>
  <div class="text_box">
    {{text_data}}
  </div>
</template>

<script>
export default {
  name: 'TextCom',
  data(){
    return {
      text_data: 'this is a nuxt ex'
    }
  },
}
</script>

<style lang="less" scoped>
.text_box{
  font-size: 20px;
  color: red;
}
</style>


