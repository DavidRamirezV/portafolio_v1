<template>
    <div class="conteiner-fluid fade-in-image">

        <div class="row separation-small">

        </div>
        <div class="row separation-medium ">
            <div class="col box-padding">

                <p data-text="David Ramírez" class="titletext2 titleanimation">
                    {{this.myname}}
                </p>

                <p class="subtitletext mx-2">
                    {{this.grade}}                    
                </p>
                <p class="basetext mx-2 type">
                    {{this.about}}  
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
    data(){
        return{
            myname: "David Ramírez",
            grade: "Ingeniero de Ejecución en Computación e Informática",
            about:"SITIO WEB EN DESARROLLO",

        }
    },
    methods:{

    }

}
</script>

<style  lang="scss">
@import url('https://fonts.googleapis.com/css2?family=DotGothic16&family=Marcellus&family=Marcellus+SC&family=Open+Sans:wght@300&display=swap');
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css");
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap');
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
.titletext2 {
    font-family: 'Poppins', serif;
    font-size: 100px;
    letter-spacing: 0.5px;
    padding-left: 0;

}
</style>
