<template lang="pug">
.contact#contact
    .container
        .redBox
            Adress 
            //- ContactForm
</template>

<script>
import Adress from './Adress'
// import ContactForm from './ContactForm'

export default {
  components: {
    Adress
    // ContactForm
  }
}
</script>

<style scoped>
.contact {
  width: 99%;
  margin-top: 15px;
}
.clear {
  width: 240px;
}
.redBox {
  background-color: #c32b27;
  display: flex;
  justify-content: center;
  padding: 25px 0 25px 0;
}
@media all and (max-width: 640px) {
  .redBox {
    flex-direction: column;
    align-items: center;
  }
  .adress {
    flex-direction: column;
  }
}
</style>
