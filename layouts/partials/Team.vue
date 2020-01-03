<template lang="pug">
.team#team
    .empty
    .container
        .mainBox
            .titleMain.fontMain
                .dotLine
                .txt
                    span Team
                .clear
        .picturesTeam
            .div
                .personBox(v-for="person in teams")
                    .img
                        img(:src="person.img")
                    .name.fontMain
                        span {{person.name}}
                    .titles
                        span {{person.title}}
                    .desc
                        span {{person.desc}}

</template>

<script>
export default {
  data() {
    return {
      teams: [
        {
          img: '@/images/luke.jpg',
          name: 'Luce Skaywalker',
          title: 'Founder & CEO',
          desc:
            'Growth strategy, finance, investors relations, product strategy.'
        },
        {
          img: '@/images/obi.jpg',
          name: 'Obi Wan Kenobi',
          title: 'Founder & Managing Partner',
          desc:
            'Growth & strategic management, product strategy, investors relations.'
        },
        {
          img: '@/images/leila.jpg',
          name: 'Leila',
          title: 'Founder & CORO',
          desc:
            'Credit risk and underwriting strategies, payments solutions. New business development.'
        },
        {
          img: '@/images/r2d2.jpg',
          name: 'R2 D2',
          title: 'Founder & Managing Partner',
          desc:
            'Growth & strategic managment, product strategy, investors relations.'
        },
        {
          img: './images/yoda.jpg',
          name: 'Yoda',
          title: 'Founder & CORO',
          desc:
            'Credit risk and underwriting strategies, payments solutions. New business development.'
        },
          {
          img: './images/vader.jpg',
          name: 'Lord Wader',
          title: 'Founder & Marketing Partner',
          desc:
            'Credit risk and underwriting strategies, payments solutions. New business development.'
        },
      ]
    }
  }
}
</script>

<style scoped>
.team {
  margin-top: 30px;
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
.empty {
  height: 100px;
}
.dotLine {
  width: 100%;
  display: flex;
  align-items: flex-end;
}
.clear {
  width: 240px;
}
.div {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  width: 77%;
}
.personBox {
  width: 28%;
  text-align: center;
  display: flex;
  flex-direction: column;
  margin: 0 25px 40px 10px;
}
.personBox .name {
  font-size: 20px;
}
.picturesTeam {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 25px;
}
.titles {
  font-size: 15px;
  color: #c32b27;
}
.desc {
  font-size: 16px;
}
img {
  width: 50%;
}
@media all and (max-width: 640px) {
  .dotLine {
    display: none;
  }
  .titleTeam {
    border-bottom: 1px dotted #c32b27;
    width: 70%;
  }
  .personBox {
    margin: 0 5px 40px 5px;
    width: 45%;
  }
  .empty {
    height: 50px;
  }
  .titleMain {
    border-bottom: 1px dotted #c32b27;
    width: 70%;
  }
}
@media all and (max-width: 420px) {
  .personBox {
    width: 100%;
  }
  .team {
    margin: 0 10px 20px 10px;
  }
}
</style>
