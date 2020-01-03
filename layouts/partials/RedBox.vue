<template lang="pug">
    .redBox
        .containerMain
            .pic
                .picture
                  img(src="@/static/images/we_are.png")
                .dotCircle
                  img(src="@/static/images/circle.svg")
                .txt
                    span.white Far far away...
                    .clear1
                    span.sm The point of using Lorem Ipsum  
                    span.sm is that it has a more-or-less
                    span.sm normal distribution of letters,
                    .clear2
                    .txt2
                      span.sm2 There are many variations   
                      span.sm2 of passages of Lorem Ipsum available.           
                      span.sm2 The point of using Lorem Ipsum           
                      span.sm2 normal distribution of letters.           
            .clear
                  
</template>

<style scoped>
.white {
  font-size: 4.4vw;
  font-family: 'Roboto';
  color: white;
  font-weight: bold;
  margin-bottom: 30px;
  margin-top: 40px;
}
.pic {
  position: relative;
}
.picture img {
  width: 100%
}
.sm {
  font-size: 24px;
  font-family: 'Roboto';
  color: white;
  font-weight: bold;
  margin-left: 50px;
  display: none;
}
.txt {
  position: absolute;
  top: 21%;
  left: 6%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.whiteBox {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
.txt2 {
  display: flex;
  flex-direction: column;
  font-size: 24px;
  font-weight: bold;
  margin-left: 50px;
}
.clear {
  width: 400px;
}
.clear1 {
  display: none;
}
.clear2 {
  height: 200px;
}
.dotCircle img {
  position: absolute;
  top: 62%;
  left: 63.7%;
  width: 25%;
}

@media all and (max-width: 1024px) {
  .white {
    font-size: 60px;
  }
}

@media all and (max-width: 896px) {
  .clear {
    width: 217px;
  }
  .clear2 {
    height: 150px;
  }
  .sm,
  .txt2 {
    font-size: 20px;
    margin-left: 40px;
  }
  .white {
    font-size: 6.4vw;
  }
}
@media all and (max-width: 768px) {
  .sm,
  .txt2 {
    font-size: 18px;
    margin-left: 10px;
  }
  .clear2 {
    height: 160px;
  }
  .white {
    margin-top: 0;
    /* font-size: 6.4vw; */
  }
}
@media all and (max-width: 640px) {
  .sm,
  .txt2 {
    font-size: 14px;
    color: black;
  }
  .txt {
    top: 6%;
  }
  .clear1 {
    display: block;
    height: 100px;
  }
  .clear2 {
    height: 45px;
  }
  .white {
    font-size: 7vw;
    margin-bottom: 0;
    margin-top: 25px;
  }
}
@media all and (max-width: 420px) {
  .txt {
    top: 10%;
    left: 1%;
  }

  .txt2 {
    color: black;
    margin-left: 10px;
    font-size: 12px;
  }
  .white {
    font-size: 28px;
    margin-bottom: 6px;
  }
  .clear1 {
    height: 30px;
  }
  .clear2 {
    height: 75px;
  }
  .sm {
    margin-left: 10px;
    font-size: 12px;
  }
}
@media all and (max-width: 350px) {
  .clear2 {
    height: 50px;
  }
}
</style>
