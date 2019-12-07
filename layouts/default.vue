<template>
  <div>
    <Nav />
    <Clear />
    <RedBox />
    <Values />
    <Product />
    <Team />
    <nuxt />
  </div>
</template>
<script>
import Nav from './partials/Nav'
import Clear from './partials/Clear'
import RedBox from './partials/RedBox'
import Values from './partials/Values'
import Product from './partials/Product'
import Team from './partials/Team'
export default {
  components: {
    Nav,
    Clear,
    RedBox,
    Values,
    Product,
    Team
  }
}
</script>
