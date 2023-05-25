<template>
  <div class="para-body">
    <!--
        
    
      
      -->
      <img src="@/assets/img/1_front.png" class="bg-rocks">
      <img src="@/assets/img/1_middle.png" class="bg-sea">
      <img src="@/assets/img/1_middle2.png" class="bg-reflection">
    <img src="@/assets/img/1_background3.png" class="bg-mountain"> 
    <img src="@/assets/img/1_backgorund2.png" class="bg-moon">
    <img src="@/assets/img/1_background.png" class="bg-image">
  </div>
</template>
  
<script>
export default {
  name: 'TopParallax'
}
</script>

<style>
.para-body {
  position: relative;
  height: 100vh;
  width: auto;
}

.bg-image {
  position: fixed;
  z-index: -1;
  /* Set rules to fill background */
  min-height: 100%;
  min-width: 1024px;
	
  /* Set up proportionate scaling */
  width: 100%;
  height: auto;
  top: 0;
  left: 0;
}

.bg-moon{
  position: absolute;
  z-index: 1;
	
  /* Set up proportionate scaling */
  width: 11%;
  height: auto;
  top: 10px;
  left: 50%;
  transform: translateX(-50%);
}

.bg-mountain{
  position: absolute;
  z-index: 2;
	
  /* Set up proportionate scaling */
  width: 100%;
  top: 100px;
  left: 0;
}

.bg-reflection{
  position: absolute;
  z-index: 5;
	
	
  /* Set up proportionate scaling */
  width: 15%;
  height: auto;
  top: 350px;
  left: 50%;
  transform: translateX(-50%);
}
.bg-sea{
  position: absolute;
  z-index: 3;
	
  /* Set up proportionate scaling */
  width: 100%;
  top: 350px;
  left: 0;
}

.bg-rocks{
  position: absolute;
  z-index: 5;
	
  /* Set up proportionate scaling */
  width: 100%;
  top: 650px;
  left: 0;
}
</style>