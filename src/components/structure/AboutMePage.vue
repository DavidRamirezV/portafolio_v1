<template>
    <div class="conteiner-fluid fade-in-image">

        <div class="row separation-small">

        </div>
        <div class="row separation-medium ">
            <div class="col box-padding">

                <p data-text="David Ramírez" class="titletext titleanimation">
                    David Ramírez

                </p>

                <p class="subtitletext mx-2">
                    Ingeniero de Ejecución en Computación e Informática
                </p>
                <p class="basetext mx-2">
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Exercitationem quasi molestias facere
                    aspernatur maiores, laboriosam itaque minus, autem assumenda labore quam. Consequuntur totam at magnam
                    maxime perferendis illum sunt odio!
           
                </p>

            </div>


        </div>
        
        <div class="row separation-small text-center">
                        

        </div>


    </div>
</template>
  
<script>
export default {
    name: 'AboutMePage',

}
</script>

<style  lang="scss">
@import url('https://fonts.googleapis.com/css2?family=DotGothic16&family=Marcellus&family=Marcellus+SC&family=Open+Sans:wght@300&family=Roboto:wght@100&display=swap');
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css");

.titletext {
    font-family: 'Marcellus SC', serif;
    font-size: 100px;
    letter-spacing: 0.5px;
    padding-left: 0;
}

.subtitletext {
    font-family: 'Marcellus', serif;
    font-size: 30px;
}

.basetext {
    font-family: 'Open Sans', sans-serif;
    font-size: 20px;
    text-align: justify;
    text-justify: inter-word;

}

</style>
