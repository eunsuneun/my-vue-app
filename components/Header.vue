<template>
  <header class="header">
      <div class="inner">
          <button class="prev-btn" @click="goToPrev()" v-if="prevBtn"></button>
          <h1 class="header__title">{{ pageTitle }}</h1>   
      </div>
  </header>
</template>

<script>
export default {
  name : 'Header',
  props : {
      pageTitle : String,
      prevBoolean: {
        default: true,
        type: Boolean
      }
  },
  data() {
    return {
      prevBtn : this.prevBoolean,
      test : false
    }
  },
  methods: {
      goToPrev() {
        window.history.back();
      },
  }
}
</script>

<style lang="scss">
@import '~/assets/scss/common';
.header { 
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: #fff; 
  border-bottom: 1px solid #e5e8ec;
  .inner {
    width: 100%;
    padding: 1rem 2rem;
    .prev-btn{
      position: absolute;
      top: 1rem;
      left: 2rem;
      width: 3rem;
      height: 3rem;
      background: url(~/static/img/prev-icon.png) no-repeat center / 1.75rem auto;
    }
  }
  &__title { 
    width: 100%;
    @include font(1.8rem, 600);
    text-align: center;
  }
  & + .content-wrap{
    margin-top: 47px;
  }
}
</style>