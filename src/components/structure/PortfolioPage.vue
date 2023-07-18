<template>
    <div class="conteiner-fluid fade-in-image">
        <!--
                src="https://thecatapi.com/api/images/get?format=src&type=gif"
            -->
        <div class="row separation-small">

        </div>

        <div class="row separation-medium">
            <div class="container-fluid ">
                <div class="row row-cols-1 row-cols-md-3 g-4 px-2 mt-2">
                    <div v-for="elemento in datoPaginados" v-bind:key="elemento.proyect_id" class="col-12 col-md-6 col-lg-4 mx-auto" style="width: 25rem;" v-on:click="goToUrl(elemento.pageurl)"  >
                        <div class="card text-center bg-dark " > 
                            <img v-bind:src=elemento.imageurl class="card-img-top" 
                                alt="...">
                            <div class="card-img-overlay h-100 d-flex flex-column justify-content-end" >
                                <h4 class="card-title text-border-custom">{{elemento.title}}</h4>
                                <p class="card-text text-border-custom">{{elemento.description}}</p>
                            </div>
                        </div>

                        
                    </div>
                </div>

                <div class="row pt-5">
                    <nav aria-label="Page navigation example">
                        <ul class="pagination  justify-content-center">
                            <li class="page-item"><a class="page-link" v-on:click="getPreviousPage()" v-bind:class=" this.paginaActual == 1 ? 'disabled':''" href="#" >Previous</a></li>
                            <li v-for="(pagina, index) in totalPaginas()" v-on:click="getDataPagina(pagina)" v-bind:key="index" v-bind:class="isActive(pagina)"
                                class="page-item"><a class="page-link" href="#">{{ pagina }}</a></li>
                            <li class="page-item"><a class="page-link" v-on:click="getNextPage()" v-bind:class=" this.paginaActual == totalPaginas() ? 'disabled':''" href="#">Next</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>


        <div class="row separation-small">
        </div>



    </div>
</template>
  
<script>

export default {
    name: 'PortfolioPage',
    props: {
        msg: String,

    },
    data() {
        return {
            lista: [{
                "proyect_id": 0,
                "title": "Pixelar imagenes",
                "year": "2023",
                "imageurl":"https://i.ibb.co/m8ydq38/Pixelart.png",
                "description": "Pequeño proyecto en Python para convertir imagenes en pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            }],
            lista_dummy: [{
                "proyect_id": 0,
                "title": "Pixelart imagenes",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes en pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 1,
                "title": "Pixelart 1",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 2,
                "title": "Pixelart 2",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 3,
                "title": "Pixelart 3",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 4,
                "title": "Pixelart 4",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 5,
                "title": "Pixelart 5",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id":6,
                "title": "Pixelart 6",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            },{
                "proyect_id": 7,
                "title": "Pixelart 7",
                "year": "2023",
                "imageurl":"https://thecatapi.com/api/images/get?format=src&type=gif",
                "description": "Pequeño proyecto en Python para convertir imagenes e pixelart",
                "pageurl": "https://colab.research.google.com/drive/1Pu3XECGbHqt_gVEeSPLsM-92pjtk2DST?usp=sharing",
                "languages": ["Python"]    
            }],
            elementosPorPagina: 6,
            datoPaginados: [],
            paginaActual: 1,
            prevDisable: true

        }
    },
    mounted() {
        this.getDataPagina(1);
    },
    methods: {
        goToUrl(url) {
            window.open(url, '_blank');
        },
        totalPaginas() {
            return Math.ceil(this.lista.length / this.elementosPorPagina)
        },
        getDataPagina(noPagina) {
            this.paginaActual = noPagina;
            this.datoPaginados = [];
            let ini = (noPagina * this.elementosPorPagina) - this.elementosPorPagina;
            let fin = (noPagina * this.elementosPorPagina);
            this.datoPaginados = this.lista.slice(ini, fin);
        },
        getPreviousPage() {
            if (this.paginaActual > 1) {
                this.paginaActual--;
            }
            this.getDataPagina(this.paginaActual);

        },
        getNextPage() {
            if (this.paginaActual < this.totalPaginas()) {
                this.paginaActual++;
            }
            this.getDataPagina(this.paginaActual);

        },
        isActive(noPagina) {
            if (noPagina == this.paginaActual) {
                return 'active';
            } else {
                return '';
            }
        },
        isPrevDisabled(noPagina){
            if (noPagina == 1) {
                return 'disabled';
            } else {
                return '';
            }

        },
        isNextDisabled(noPagina){
            if (noPagina == this.totalPaginas()) {
                return 'disabled';
            } else {
                return '';
            }

        }

    }
}
</script>

<style  lang="scss">
.text-border-custom {
    text-shadow: 0 0 3px #240808, 0 0 5px #02020a;
}
.card{
    cursor: pointer;
    transition: all 0.3s;
}
.card:hover{
    transform: scale(1.05);
}
</style>