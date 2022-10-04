<template>
  <div class="wrap">
    <Nuxt />
  </div>
</template>
<script>
  import { commonFn } from '~/assets/js/common.js';
  export default {
    head () {
      return {
        title: 'my-vue-app',
        meta: [
          { 
            name: 'my-vue-app', 
            content: 'my-vue-app' 
          }
        ]
      }
    },
    mounted(){
      commonFn();
    },
  }
</script>
<style lang="scss">
  @import '~/assets/scss/common';
</style>