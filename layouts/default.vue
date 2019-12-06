<template>
  <div>
    <Nav />
    <Clear />
    <RedBox />
    <Values />
    <Product />
    <nuxt />
  </div>
</template>
<script>
import Nav from './partials/Nav'
import Clear from './partials/Clear'
import RedBox from './partials/RedBox'
import Values from './partials/Values'
import Product from './partials/Product'
export default {
  components: {
    Nav,
    Clear,
    RedBox,
    Values,
    Product,
  }
}
</script>
