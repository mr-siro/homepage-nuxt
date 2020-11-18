<template>
  <div id="app">
    <div class="home-wrapper">
      <div class="home-header">
        <DefaultHeader/>
      </div>
      <div class="home-content">
        <Nuxt />
      </div>
      <div class="home-footer">
        <DefaultFooter/>
      </div>
    </div>
    <BackToTop title="Top" />
  </div>
</template>
<script>
import DefaultHeader from './header/DefaultHeader'
import DefaultFooter from './footer/DefaultFooter'
import BackToTop from '@/components/button/BackToTop'
export default {
  components:{
    DefaultHeader,
    DefaultFooter,
    BackToTop
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.home-wrapper {
  display: grid;
  grid-template-columns: 3fr;
}
.home-header, .home-content, .home-footer {
  grid-column: 1/3;
  width: 100%;
}
</style>
