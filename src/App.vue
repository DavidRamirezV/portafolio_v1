<template>
  <FloatingActionButton v-on:handlerData="updateDisplay"/>
  <div class="container-fluid body-default">
    <div class="row ">
      <div class="col-2 sidebar_st">
        <!--
  Top
 -->
        <div class="row pt-5 pb-3 mt-3 mx-3">
          <img src="./assets/img/profile_6.png" id="profileimg" class="card-img-top rounded-circle zoom" alt="Profile">
          <h4 class="text-center pt-3">David Ramírez</h4>
          <h6 class="text-center text-muted">Ingeniero Informático</h6>
        </div>

        <div class="row">
          <div class="card-footer text-muted py-3">
            <div class="row text-center mx-4">
              <div class="col">
                <a href="https://www.linkedin.com/in/david-antonio-ramirez-vicuna/" target="_blank">
                  <img src="./assets/img/linkedin.png" alt="Linkedin" height="50px" class="zoom">
                </a>
              </div>
              <div class="col">
                <a href="https://github.com/DavidRamirezV" target="_blank">
                  <img src="./assets/img/github.png" alt="GitHub" height="50px" class="zoom">
                </a>
              </div>
            </div>
          </div>       
        </div>

        <!--
  Middle
 -->

        <div class="pt-1">
          <div class="pice-border my-3" id="sidebtn1">
            <a class="btn" @click="displayHandler(1)"> SOBRE MÍ</a>
          </div>
          <div class="pice-none my-3" id="sidebtn2">
            <a class="btn" @click="displayHandler(2)"> EDUCACIÓN</a>
          </div>
          <div class="pice-none my-3" id="sidebtn3">
            <a class="btn" @click="displayHandler(3)"> CARRERA</a>
          </div>
          <div class="pice-none my-3" id="sidebtn4">
            <a class="btn" @click="displayHandler(4)"> PORTAFOLIO</a>
          </div>
          <div class="pice-none my-3" id="sidebtn5">
            <a class="btn" @click="displayHandler(5)"> CONTACTO</a>
          </div>
          

        </div>
        <!--
Footer
 -->
 
      </div>

      <div class="col-10">
        <AboutMePage v-if="display_1" />
        <EducationPage v-else-if="display_2" />
        <CareerPage v-else-if="display_3" />
        <PortfolioPage v-else-if="display_4" />
        <ContactPage v-else-if="display_5" />
        <div v-else>Nothing to display</div>
      </div>


    </div>

  </div>

  <!--
      <HelloWorld msg="Welcome to Your Vue.js App" />
    -->
</template>

<script>
import $ from 'jquery'
import AboutMePage from './components/structure/AboutMePage.vue'
import EducationPage from './components/structure/EducationPage.vue'
import CareerPage from './components/structure/CareerPage.vue'
import PortfolioPage from './components/structure/PortfolioPage.vue'
import ContactPage from './components/structure/ContactPage.vue'
import FloatingActionButton from './components/others/FloatingActionButton.vue'
//import BoostrapTest from './components/BoostrapTest.vue'

export default {

  name: 'App',
  data() {
    return {
      display_1: true,
      display_2: false,
      display_3: false,
      display_4: false,
      display_5: false

    }
  },
  components: {
    AboutMePage,
    EducationPage,
    CareerPage,
    PortfolioPage,
    ContactPage,
    FloatingActionButton

  },
  methods: {

   

    displayHandler: function (pressed) {
      this.display_1 = false;
      this.display_2 = false;
      this.display_3 = false;
      this.display_4 = false;
      this.display_5 = false;
      $('#sidebtn1,#sidebtn2,#sidebtn3,#sidebtn4,#sidebtn5').attr('class', 'pice-none my-3');

      if (pressed == 1) {
        if (this.display_1 == false) {
          $('#sidebtn1').attr('class', 'pice-border my-3')
          this.display_1 = true;
        }

      } else if (pressed == 2) {
        if (this.display_2 == false) {
          $('#sidebtn2').attr('class', 'pice-border my-3')
          this.display_2 = true;
        }
      }
      else if (pressed == 3) {
        if (this.display_3 == false) {
          $('#sidebtn3').attr('class', 'pice-border my-3')
          this.display_3 = true;
        }
      }
      else if (pressed == 4) {
        if (this.display_4 == false) {
          $('#sidebtn4').attr('class', 'pice-border my-3')
          this.display_4 = true;
        }
      }
      else if (pressed == 5) {
        if (this.display_5 == false) {
          $('#sidebtn5').attr('class', 'pice-border my-3')
          this.display_5 = true;
        }
      }

    },

    updateDisplay(newData){
      this.displayHandler(newData);
    },
  }
}


</script>

<style lang="scss">
@import './assets/styles/main.scss';
</style>