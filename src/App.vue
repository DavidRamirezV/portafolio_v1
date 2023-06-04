<template>
  <div class="container-fluid body-default">

    <div class="row ">
      <div class="col-2 sidebar_st">
        <!--
  Top
 -->
        <div class="row pt-5 pb-3 mt-3 mx-3">
          <img src="./assets/img/profile.gif" id="profileimg" class="card-img-top rounded-circle" alt="Profile">
          <h4 class="text-center pt-3">David Ramírez</h4>
          <h6 class="text-center text-muted">Ingeniero Informático</h6>
        </div>
        <!--
  Middle
 -->

        <div class="pt-1">
          <div class="pice-border my-3">
            <a class="btn" href="#"  ref="sidebtn1"  @click="displayHandler(1)"> SOBRE MÍ</a>
          </div>
          <div class="pice-border my-3">
            <a class="btn" href="#"  ref="sidebtn2" @click="displayHandler(2)"> EDUCACIÓN</a>
          </div>
          <div class="pice-border my-3">
            <a class="btn" href="#"> CARRERA</a>
          </div>
          <div class="pice-border my-3">
            <a class="btn" href="#"> PORTAFOLIO</a>
          </div>
          <div class="pice-border my-3">
            <a class="btn" href="#"> CONTACTO</a>
          </div>

        </div>
        <!--
Footer
 -->
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

      </div>

      <div class="col-10">
        <AboutMePage v-if="display_1"/>
        <EducationPage v-else-if="display_2"/>
        <div v-else>Nothing to display</div>
      </div>


    </div>

  </div>

  <!--
      <HelloWorld msg="Welcome to Your Vue.js App" />
    -->
</template>

<script>
import AboutMePage from './components/structure/AboutMePage.vue'
import EducationPage from './components/structure/EducationPage.vue'
//import BoostrapTest from './components/BoostrapTest.vue'

export default {
  
  name: 'App',
  data(){
    return{
      display_1 :true,
      display_2 :false,

    }
  },
  components: {
    AboutMePage,
    EducationPage

  },
  methods: {
   
    displayHandler: function (pressed){
    
      if (pressed==1){
        if (this.display_1 == false ){
          this.display_1 = true;
          this.display_2 = false;
        }
        
      }else if (pressed==2){
        if (this.display_2 == false ){
        this.display_1 = false;
        this.display_2 = true;
        }
      }

      //console.log("d1: " + this.display_1 +" d2:" + this.display_2 );
      
    }
  }
}


</script>

<style lang="scss">
.body-default {
  background-color: #272727;
  color: #fff;
  height: 100vh;
}

//SIDEBAR

.sidebar_st {
  background-color: #1f1f1f;
  height: 100vh;
}

//RGB LIGHT EFFECT
.pice-border {
  background: rgb(250, 6, 252);
  background: linear-gradient(90deg, rgba(250, 6, 252, 1) 0%, rgba(158, 61, 255, 1) 25%, rgba(0, 249, 255, 1) 50%, rgba(158, 61, 255, 1) 75%, rgba(250, 6, 252, 1) 100%);
  animation: gradient 55s linear infinite;
  width: 100%;
  height: 3.5em;
  max-height: 4em;
  min-height: 3em;
  position: relative;
  border-radius: 6.5px;
}

.pice-border::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  background: inherit;
  filter: blur(6px);
}

.pice-border .btn {
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #000000;
  width: 99%;
  height: 96%;
  background-image: linear-gradient(180deg, #272727 0%, #1f1f1f 100%);
  text-align: center;
  text-decoration: none;
  color: #fff;
  letter-spacing: 1px;
  padding-top: 0.85em;
  padding-bottom: 0.85em;

}

.pice-border .btn:hover {
  color: #fff;
  font-weight: bold;


}


@keyframes gradient {
  0% {
    background-position: 0 0;
  }

  50% {
    background-position: 50em 50em;
  }

  100% {
    background-position: 1em 5em;
  }

}

//ZOOM
.zoom {
  transition: transform .2s;
}

.zoom:hover {
  -ms-transform: scale(1.2);
  /* IE 9 */
  -webkit-transform: scale(1.2);
  /* Safari 3-8 */
  transform: scale(1.2);
}


//photo morph
</style>