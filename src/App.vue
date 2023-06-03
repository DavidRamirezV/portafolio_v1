<template>
  <div class="container-fluid">

    <div class="row">
      <div class="col-2 sidebar_st">

        <img src="https://i.ibb.co/PtSkvSQ/katwall.jpg" class="card-img-top" alt="Preview">

        <div class="pice-border">
          <a class="btn" href="#"> TESTING 1</a>
        </div>
        <div class="pice-border">
          <a class="btn" href="#"> TESTING 2</a>
        </div>
        <div class="pice-border">
          <a class="btn" href="#"> TESTING 3</a>
        </div>
        <div class="pice-border">
          <a class="btn" href="#"> test 4</a>
        </div>
        <div class="pice-border">
          <a class="btn" href="#"> test 5</a>
        </div>


        <div class="card-footer text-muted">
          2 days ago
        </div>


      </div>


      <div class="col-10">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque ad dolore qui, repudiandae consequatur dolorum
        quidem nihil neque iusto consectetur, veritatis provident asperiores, molestias officiis sapiente facere fuga
        veniam maiores?

        
      </div>



    </div>

  </div>

  <!--
      <img alt="Vue logo" src="./assets/logo.png">
      <HelloWorld msg="Welcome to Your Vue.js App" />
    -->
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import BoostrapTest from './components/BoostrapTest.vue'
//import ImageCarousel from './components/Images/ImageCarousel.vue'

export default {
  name: 'App',
  components: {

  }
}
</script>

<style lang="scss">
.sidebar_st {
  background-color: #1f1f1f;
  height:100vh;
  ul {
    li {
      background-color: rgb(141, 114, 139);
    }
  }
}

.pice-border {
  background: rgb(250, 6, 252);
  background: linear-gradient(90deg, rgba(250, 6, 252, 1) 0%, rgba(158, 61, 255, 1) 25%, rgba(0, 249, 255, 1) 50%, rgba(158, 61, 255, 1) 75%, rgba(250, 6, 252, 1) 100%);
  animation: gradient 55s linear infinite;
  width: 100%;
  height: 2.5em;
  max-height: 4em;
  min-height: 2.5em;
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
  background-image: linear-gradient(180deg, #272727 0%, #1f1f1f 100%);
  text-align: center;
  text-decoration: none;
  color: #fff;
  letter-spacing: 1px;

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
</style>