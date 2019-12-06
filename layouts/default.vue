<template>
  <div>
    <Nav />
    <RedBox />
    <nuxt />
  </div>
</template>
<script>
import Nav from './partials/Nav'
import RedBox from './partials/RedBox'
export default {
  components: {
    Nav,
    RedBox,
  }
}
</script>
