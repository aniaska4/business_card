<template lang="pug">
    .nav
        .containerMain
            nav.mainNav
                .pic
                    a(href="/")
                      img(src="@/static/images/images.jpg")
                .navigation
                    ul
                        li(v-for="(nav, index) in navs", :key="index" nuxt-link :to="nav.link") 
                          a(:href="nav.href") {{nav.name}}
            //- Slide(right)
            //-   nav.menu_vertical
            //-     nav
            //-       ul
            //-         li(v-for="(nav, index) in navs", :key="index" nuxt-link :to="nav.link") 
            //-           a(:href="nav.href") {{nav.name}}
</template>
<script>
// import { Slide } from 'vue-burger-menu'
export default {
//   name: 'Nav',
  components: {
    // Slide
  },
  data() {
    return {
      navs: [
        { link: 'about', name: 'About us', href: '#about' },
        { link: 'product', name: 'Product', href: '#product' },
        { link: 'team', name: 'Team', href: '#team' },
        { link: 'locations', name: 'Locations', href: '#locations' },
        { link: 'contact', name: 'Contact', href: '#contact' }
      ]
    }
  }
}
</script>
<style scoped>
    .nav {
    width: 100%;
    height: 87px;
    display: flex;
    align-items: center;
    margin-bottom: 18px;
    position: fixed;
    background-color: #fff;
    z-index: 1000;
    }

  .bm-overlay {
    background: white !important;
  }
  .bm-menu {
    background-color: #ffffffe3 !important;
  }
  .bm-cross {
    background-color: #c32b27 !important;
  }
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  
  .containerMain {
      
    font-family: 'Roboto', sans-serif !important;
    color: black !important;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
  }
  .fontMain {
    font-size: 24px;
    font-weight: bold;
  }

.pic img {
  width: 170px;
  margin-right: 105px;
}
.mainNav {
  width: 100%;
  display: flex;
  justify-content: space-around;
}

.mainNav ul {
  list-style-type: none;
  display: flex;
  flex-direction: row;
  justify-content: left;
  color: black;
  font-weight: 400;
}
ul li {
  margin: 0 25px 0 15px;
  cursor: pointer;
}
.navigation {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.menu_mob {
  display: none;
  position: absolute;
  right: 0;
  cursor: pointer;
  z-index: 2000;
}
.menu_vertical {
  z-index: 1000;
  width: 100%;
  margin: 0 auto;
  float: center;
  padding-bottom: 15px;
  width: 70%;
}
.menu_vertical ul {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.menu_vertical ul li {
  line-height: 2;
  text-transform: uppercase;
}
.menu_vertical ul li a {
  color: #c32b27;
  font-weight: 700;
}
.navigation ul li a {
  color: black;
}

.logo {
  float: left;
  display: inline;
  margin: 30px 0 0 60px;
}

@media all and (max-width: 1024px) {
  .white {
    font-size: 4.5vh;
  }
  .sm {
    font-size: 1.3vh;
  }
  .txt2 {
    font-size: 1.3vh;
  }
}
@media all and (max-width: 768px) {
  ul li {
    margin: 0 20px 0 0;
    cursor: pointer;
  }
  .pic img {
    margin-right: 60px;
  }
}

@media all and (max-width: 640px) {
  .navigation {
    display: none;
  }
  .menu_mob {
    display: inline;
  }
  .mainNav {
    justify-content: space-between;
  }
  .nav {
    height: 85px;
  }
}
</style>
