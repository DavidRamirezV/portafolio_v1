<template>
    <div class="conteiner-fluid fade-in-image">

        <div class="row separation-small">

        </div>
        <div class="row separation-medium ">
            <div class="col box-padding">

                <p data-text="David Ramírez" class="titletext2">
                    {{ this.myname }}
                </p>

                <p class="subtitletext mx-2">
                    {{ this.grade }}
                </p>
                <p class=" mx-2 " style="display: inline;">
                    <i class="warningtext bi bi-exclamation-triangle-fill px-3"> <span class="px-3">{{ this.warning }}</span></i>
                </p>
                <div class="basetext mx-2 my-1">
                    <p>
                        ¡Hola! Soy un joven profesional recién titulado de la carrera de Ingeniería de Ejecución en
                        Computación e Informática de la Universidad de Santiago de Chile (USACH). Mi interés en la
                        informática esta orientada al desarrollo full stack de aplicaciones web.
                    </p>
                    <p>
                        A lo largo de mi formación, he tenido la fortuna de trabajar en diversos proyectos de desarrollo de
                        software y aplicaciones web. Mi experiencia abarca tanto el diseño y desarrollo de la parte frontal
                        (frontend), la construcción sólida del backend y el desarrollo de bases de datos relacionales y no
                        relacionales.
                    </p>
                    <p>
                        Mi dedicación a la tecnología y mi afán por superar desafíos me impulsan a estar en constante
                        búsqueda de mejoras y crecimiento profesional. Estoy ansioso por aplicar mis habilidades en un
                        entorno laboral, donde pueda contribuir significativamente y seguir aprendiendo en el proceso.
                    </p>
                    <p>
                        Aprecio tu interés en revisar mi perfil. Estoy entusiasmado por la posibilidad de unirme a un equipo
                        que valore la innovación y la dedicación. Si necesitas más detalles o deseas conocer más acerca de
                        mí, no dudes en contactarme.
                    </p>
                </div>


            </div>

        </div>

        <div class="row separation-small text-center">


        </div>


    </div>
</template>
  
<script>
export default {
    name: 'AboutMePage',
    data() {
        return {
            myname: "David Ramírez",
            grade: "Ingeniero de Ejecución en Computación e Informática",
            warning: "SITIO WEB EN DESARROLLO",

        }
    },
    methods: {

    }

}
</script>

<style  lang="scss"></style>