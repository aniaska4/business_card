<template lang="pug">
.titleContact
    .txt
        span Contact
    .desc.fontMain
        span We offer a comprehensive credit product
        span to finance our Customers needs in every aspect.
    .adress
        .boxContact
            .one
                span.name Galaxies Relations
                .tel
                  img(src="@/static/images/tel.png")
                  span mob/whatsapp: (0048) 666 666 666
                .mail
                  img(src="@/static/images/mail.png")
                  span e-mail: stars.wars@gmail.com
            .two
                span.name-1 Stars Wars company
                span Head office address:
                span.adress-1 Galaxies street 13
                span.adress-1 02-000 Warsaw
                span.adress-1 Poland
</template>

<script>
export default {}
</script>

<style scoped>
.txt {
  color: white;
  padding-left: 0;
}
.titleContact {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 70%;
}
.desc {
  display: none;
  margin-left: 35px;
}
.txt {
  display: flex;
  flex-direction: column;
  margin-bottom: 25px;
}
.desc {
  color: white;
}
.adress {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: white;
  margin-left: 35px;
}
.one,
.two {
  display: flex;
  flex-direction: column;
  margin-bottom: 30px;
}
.space {
  height: 15px;
}
.boxContact {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.name {
  font-size: 32px !important;
  font-weight: bold;
}
.name-1 {
  font-size: 16px;
}
.one span,
.two span {
  line-height: 2;
  font-size: 19px;
}
img {
  margin-right: 10px;
  width: 35px;
}
.tel,
.mail {
  display: flex;
  margin-top: 15px;
}

@media all and (max-width: 1024px) {
  .boxContact {
    width: 100%;
    margin-right: 20px;
  }
}
@media all and (max-width: 968px) {
  .boxContact {
    flex-direction: column;
  }
}
@media all and (max-width: 640px) {
  .boxContact {
    flex-direction: column;
    justify-content: center;
  }
  .txt {
    font-size: 45px;
    margin-bottom: 15px;
  }
  .titleContact {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 90%;
    margin-left: 15px;
  }
  .one,
  .two {
    font-size: 16px;
    margin-bottom: 25px;
  }
  .one span,
  .two span {
    line-height: 1.5;
    font-size: 16px;
  }
  .name {
    font-size: 24px;
  }
  img {
    height: 40px;
  }
  .adress-1 {
    margin-top: 7px;
  }
}
@media all and (max-width: 420px) {
  .adress {
    margin-left: 0;
  }
  img {
    margin-right: 0;
  }
}
</style>
