.<template lang="pug">
.value#about
    .empty
    .container
        .mainBox
            .titleMain.fontMain
                .dotLine
                .txt
                    span Pillars
                .clear
            .values
                .picValues(v-for="value in values")
                    .img
                        img(:src="'/business_card' + value.img")
                    .titleValues2.fontMain
                        span {{value.title}}
                    .txtDescription
                        span {{value.txt}}

</template>

<script>
export default {
  data() {
    return {
      values: [
        {
          title: 'Luke',
          img: '/images/simplicity.svg',
          txt:
            'Lucas ipsum dolor sit amet darth antilles jabba dagobah yoda ponda hoth dantooine solo dooku.'
        },
        {
          title: 'Han Solo',
          img: '/images/head.svg',
          txt:
            'Solo padmé moff dooku solo. Twilek aayla moff luke.'
        },
        {
          title: 'Ahsoka',
          img: '/images/service.svg',
          txt:
            'Ahsoka amidala lars antilles c-3p0 cade yoda hutt. Calrissian mara lobot boba darth.'
        },
        {
          title: 'Leila',
          img: '/images/mobile.svg',
          txt: 'Leia palpatine binks watto mon dagobah. Jabba coruscant antilles jabba ewok anakin.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.value {
  margin-top: 50px;
}
.titleMain,
.titleValues2 {
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  width: 100%;
  margin: 15px 0 30px 0;
  font-weight: bold;
  text-align: center;
  justify-content: center;
  line-height: 1;
  height: 50px;
}
.txt {
  align-items: flex-end;
}
.empty {
  height: 140px;
}
.values {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 79%;
  margin-top: 30px;
}
.picValues {
  width: 450px;
  margin-bottom: 60px;
}
.clear {
  width: 250px;
}
.txtDescription {
  text-align: center;
  line-height: 1.2;
}
.img {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 70px;
}
.img img {
  width: 30%;
}
@media all and (max-width: 420px) {
  .value {
    margin: 0 10px 20px 10px;
  }
  .empty {
    height: 140px;
  }
}
@media all and (max-width: 640px) {
  .values {
    width: 95%;
  }
  .titleMain {
    border-bottom: 1px dotted #c32b27;
    width: 70%;
    justify-content: flex-start;
  }
}
@media all and (max-width: 768px) {
  .empty {
    height: 100px;
  }
}
@media all and (max-width: 1024px) {
  .empty {
    height: 190px;
  }
}
</style>
