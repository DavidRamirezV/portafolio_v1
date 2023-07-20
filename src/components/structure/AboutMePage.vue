<template>
    <div class="conteiner-fluid fade-in-image">

        <div class="row separation-small">

        </div>
        <div class="row separation-medium ">
            <div class="col box-padding">

                <p data-text="David Ramírez" class="titletext2">
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
</style>