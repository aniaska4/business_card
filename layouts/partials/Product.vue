<template lang="pug">
.product#product
    .empty
    .container
        .mainBox
          .titleMain
              .clear
              .txt
                span Service
              .dotLine
                //- img(src="@/static/images/line2.svg")
          .productDescription
              .clearBox
              .txtmain.fontMain
                span Momentum furnunculus totalus evanesco charm patronum mobilicorpus mortis stupefy. 
                  | incantartem impedimenta. Ennervate totalus mortis relashio cruciatus.
                  | immobulus reducto silencio. Riddikulus deletrius mortis wingardium legilimens.
                  | Nox lumos rennervate mobilicorpus.
                  | Evanesco lumos aparecium lacarnum incantartem inflamarae.                     
              .clearBox
              .picHand
                //- img(src="@/static/images/hand.svg")
          .productPoint
            .zone
              .clearBox2
              .titleProduct.fontMain
                span Our go to product:
              .points
                .span(v-for="point in firstPoints")
                  .img
                  li {{point}}
              .points 
                .span(v-for="point in secondPoints")
                  .img
                  li {{point}}
</template>

<script>
export default {
  data() {
    return {
      firstPoints: [
        'Engorgio lumos tergeo mobilicorpus locomotor inflamarae',
        'Legilimens petrificus totalus lacarnum.',
        'Hover rictusempra nox muffliato stupefy.'
      ],
      secondPoints: [
        'Mobilicorpus wingardium lacarnum immobilus.',
        'Mobilicorpus quietus disapparate lumos locomotor'
      ]
    }
  }
}
</script>

<style scoped>
.empty {
  height: 75px;
}
.product {
  margin-top: 15px;
}
.titleMain {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.titleValues {
  font-size: 80px;
  font-weight: bold;
  margin-right: 20px;
}
.clear {
  width: 240px;
}
.dotLine img {
  padding-bottom: 27px;
}
.productDescription {
  display: flex;
  flex-direction: row;
  margin-top: 28px;
  margin-bottom: 85px;
}
.txt {
  padding-left: 0;
}
.txtmain {
  width: 55%;
  display: flex;
  flex-direction: column;
  line-height: 1.3;
  text-align: justify;
}
.picHand {
  margin-left: 30px;
}
.picHand img {
  width: 50%;
  height: 81%;
}
.clearBox {
  width: 157px;
}
.clearBox2 {
  width: 15px;
}
.productPoint {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.zone {
  display: flex;
  margin-left: 10%;
}
.titleProduct {
  width: 23%;
  display: flex;
  align-items: center;
}
.points {
  width: 38%;
  display: flex;
  flex-direction: column;
  border-left: 1px dashed #da2228;
  padding-left: 20px;
  padding-right: 38px;
  line-height: 1.3;
}
.points li {
  margin-bottom: 25px;
  list-style-type: none;
}
.span .img {
  display: none;
}
@media all and (max-width: 1024px) {
  .zone {
    margin-left: 2%;
  }
  .clearBox2 {
    display: block;
    width: 157px;
  }
  .productDescription {
    margin-right: 15px;
  }
}
@media all and (max-width: 968px) {
  .picHand {
    display: none;
  }
  .txtmain {
    width: 100%;
    margin: 0 50px 0 50px;
    display: block;
    text-align: justify;
  }
  .zone {
    flex-direction: column;
    width: 84%;
  }
  .titleProduct {
    width: 100%;
    margin-bottom: 25px;
  }
  .points {
    border: none;
    width: 100%;
    padding-left: 7px;
  }
  .points li {
    margin-bottom: 10px;
    width: 100%;
  }
  .span {
    display: flex;
    line-height: 1.5;
  }
  .span .img {
    display: block;
    width: 22%;
    margin-bottom: 5px;
    background-size: 30px 28px;
    background-image: url('/business_card/images/circle_red.svg');
    background-repeat: no-repeat;
  }
}
@media all and (max-width: 640px) {
  .titleMain {
    border-bottom: 1px dotted #c32b27;
    width: 70%;
  }
  .productDescription {
    margin-bottom: 30px;
  }
  .clearBox {
    width: 0;
  }
  .clearBox2 {
    width: 0;
  }
  .span img {
    width: 10%;
  }
}
@media all and (max-width: 420px) {
  .product {
    margin: 0 10px 20px 10px;
  }
  .txtmain {
    text-align: justify;
    display: block;
    margin: 0 15px 0 15px;
  }
  .zone {
    width: 100%;
  }
  .span img {
    margin-right: 15px;
  }
}
</style>
