<template>
    <div class="conteiner-fluid">
        <p class="body-animation">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Deserunt, consectetur consequatur hic eius quae
            architecto est iste labore delectus mollitia, repellendus odit possimus atque culpa earum. Aliquam facilis
            reiciendis tempora.

        </p>

        <div class="pice-border1 my-3">
            <a class="btn"> SOBRE MÍ</a>
        </div>

        <div class="pice-border1 my-3" >
            <a class="btn"> EDUCACIÓN</a>
        </div>

    </div>
</template>
  
<script>
export default {
    name: 'AboutMePage',

}
</script>

<style  lang="scss">
.body-animation {
    animation: fadeInAnimation ease 3s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}

@keyframes fadeInAnimation {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

</style>