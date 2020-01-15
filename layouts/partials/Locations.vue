<template lang="pug">
.locations#locations
    .empty
    .container
        .mainBox
            .titleMain.fontMain
                .clear
                .txt
                    span Locations
                .dotLine
            .imageMap
                .img
                .countryImg
                    .country(v-for="country in countrys" :key="country.class")
                        .flag(:class="country.class" @mouseover="mouseover(country.boxClass)" @mouseleave="mouseleave")
                            img(:src="'/business_card' + country.img" )
                .countryInfo
                    .info
                        .boxCountry(:class="info.boxClass" :style='isVisible')
                          .name {{info.name}}
                          .spans
                            span description: {{info.description}}
                            span Amounts: {{info.goLive}}
                            span Product: {{info.product}}
                            span Adress: {{info.applications}}
                            span Phone: {{info.verification}}
                            span Payments: {{info.payments}}
                          .wwwPage {{info.www}}

</template>

<script>
export default {
  data() {
    return {
      info: {
        class: '',
        boxClass: '',
        name: '',
        description: '',
        goLive: '',
        product: '',
        applications: '',
        verification: '',
        payments: '',
        www: ''
      },
      countrys: {
        pl: {
          img: '/images/poland.svg',
          ref: 'Pl',
          class: 'poland',
          boxClass: 'pl',
          name: 'Poland',
          description: 'Lorem ipsum dolor sit amet',
          product: 'Sed nibh purus',
          goLive: '500 to 3000 EUR 12-48 months',
          applications: 'online',
          verification: 'online',
          payments: 'online',
          www: 'www.lucas.pl'
        },
        mx: {
          img: '/images/mexico.svg',
          ref: 'Mx',
          class: 'mexico',
          boxClass: 'mx',
          name: 'Mexico',
          description: 'Lorem ipsum dolor sit amet',
          product: 'Sed nibh purus',
          goLive: '100 to 700 EUR 3-12 months',
          applications: 'online',
          verification: 'online',
          payments: 'online',
          www: 'www.leila.mx'
        },
        br: {
          img: '/images/brazil.svg',
          ref: 'Br',
          class: 'brasil',
          boxClass: 'br',
          name: 'Brasil',
          description: 'Lorem ipsum dolor sit amet',
          product: 'Sed nibh purus',
          goLive: '100 to 700 EUR 3-12 months',
          applications: 'online',
          verification: 'online',
          payments: 'online',
          www: 'www.yoda.br'
        }
      }
    }
  },
  computed: {
    isVisible() {
      if (this.info.boxClass !== '') {
        return { display: 'flex' }
      } else {
        return { display: 'none' }
      }
    }
  },
  methods: {
    mouseover(boxClass) {
      Object.assign(this.info, this.countrys[boxClass])
    },
    mouseleave() {
      this.info.boxClass = ''
    }
  }
}
</script>

<style scoped>
.locations {
  margin-top: 10px;
}
.titleMain {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  width: 100%;
  height: 75px;
  margin-bottom: 10px;
  font-weight: bold;
}
.clear {
  width: 240px;
}
.imageMap {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  margin-top: 30px;
}
/* .imageMap img {
  width: 100%;
} */
.img {
  width: 80%;
  background-image: url('/business_card/images/map.svg');
  background-repeat: no-repeat;
}
.flag img {
  width: 5%;
  position: absolute;
}
.poland img {
  top: 32%;
  left: 49%;
}
.mexico img {
  top: 40%;
  left: 25%;
}
.brasil img {
  top: 62%;
  left: 36%;
}
.name,
.wwwPage {
  width: 50%;
  background-color: #c32b27;
  color: white;
  height: 30px;
}
.name {
  border-radius: 10px 10px 10px 0;
  position: absolute;
  top: -5%;
  left: 0;
  z-index: 1000;
  text-align: center;
}
.wwwPage {
  border-radius: 10px 0 10px 10px;
  position: absolute;
  top: 89%;
  left: 50%;
  z-index: 1000;
  text-align: center;
}
.boxCountry {
  width: 300px;
  display: none;
  flex-direction: column;
  position: relative;
  background-color: #fff;
  box-shadow: 0 3px 12px;
}
.spans {
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  padding: 20px 10px 30px 10px;
}
.br {
  position: absolute;
  top: 51%;
  left: 44%;
  display: none;
}
.pl {
  position: absolute;
  top: 23%;
  left: 61%;
  display: none;
}
.mx {
  position: absolute;
  top: 51%;
  left: 7%;
  display: none;
}
.hovered {
  display: block;
}
@media all and (max-width: 640px) {
  .titleMain {
    border-bottom: 1px dotted #c32b27;
    width: 70%;
  }
}
@media all and (max-width: 968px) {
  .countryInfo {
    display: none;
  }
}
@media all and (max-width: 420px) {
  .locations {
    margin: 0 10px 20px 10px;
  }
  .empty {
    height: 60px;
  }
}
</style>
