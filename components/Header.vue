<template>
  <header class="header">
      <div class="inner">
          <button class="prev-btn" @click="goToPrev()"></button>
          <h1 class="header__title">{{ gnbTxt }}</h1>   
      </div>
  </header>
</template>

<script>
export default {
  name : 'Header',
  props : {
      gnbTxt : String
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
}
</style>