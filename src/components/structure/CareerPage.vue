<template>
  <div class="conteiner-fluid fade-in-image">

    <div class="row separation-small">

    </div>
    <div class="row separation-medium">
      <div class="col">


        <div class="alt-vtl">
          <div class="alt-event">
            <p class="title_1"> (PROYECTO) Endpoint para la generación de discursos hablados</p>
            <p class="subtitle_1">Abril, 2023</p>
            <p class="txt">Proyecto de tesis que utilizaba Go + Gin en combinación con Google Cloud text-to-speech para la
              creación de un servicio API REST.</p>
            <hr>
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" height="50px" />
            +
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg"  height="50px"/>
          </div>
          <div class="alt-event right">
            <p class="title_1">(PROYECTO) Planificación docente del Departamento de Ingeniería Informática</p>
            <p class="subtitle_1">Noviembre, 2022</p>
            <p class="txt">Desarrollo de un sitio web basado en un modelo de procesos enfocado en la planificación docente del deparatamento de
              informatica de mi universidad.</p>
            <hr>
            
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-plain-wordmark.svg" height="50px"/>
          
            +

            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rails/rails-plain-wordmark.svg" height="50px" />
            +
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-plain-wordmark.svg"
              height="50px" />



          </div>
        </div>
      </div>


    </div>
    <div class="row separation-small">

    </div>


  </div>
</template>
  
<script>
export default {
  name: 'CareerPage',
  props: {
    msg: String
  }
}
</script>

<style  lang="scss">
$magenta_custom: rgb(250, 6, 252, );
$purple_custom: rgb(158, 61, 255);
$cian_custom: rgb(0, 249, 255);
$dark_custom: #1f1f1f;
$darklight_custom: #272727;


/* (A) TIMELINE CONTAINER */
.alt-vtl {
  /* (A1) RELATIVE POSITION REQUIRED TO PROPERLY POSITION THE TIMELINE */
  position: relative;

  /* (A2) WIDTH RESTRICTION & CENTER ON PAGE */
  max-width: 1000px;
  margin: 0 auto;
}

/* (B) DRAW TIMELINE USING ::BEFORE */
.alt-vtl::before {
  /* (B1) VERTICAL LINE */
  content: "";
  width: 5px;
  background-color: $purple_custom;

  /* (B2) POSITION IN THE MIDDLE */
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
}

/* (C) EVENTS */
div.alt-event {
  /* (C1) COSMETICS */
  background-color: $dark_custom;
  box-shadow: 8px 8px 5px 1px #302636;
  border-radius: 6px;

  /* (C2) DIMENSIONS */
  padding: 20px 30px;
  width: 45%;
  margin-bottom: 10px;

  /* (C3) POSITION - DEFAULT LEFT SIDE */
  position: relative;
  left: 0;
}

/* (C4) CHANGE EVENT POSITION TO RIGHT SIDE */
div.right {
  left: 55%;
}

/* (D) COSMETICS FOR EVENT DATE & TEXT */
p.title_1 {
  font-size: 1.1em;
  font-weight: 700;
  color: white;
  margin-bottom: 8px;

}

p.subtitle_1 {
  color: #6c757d !important;
  margin: 0px;
}

p.txt {
  text-align: justify;
  text-justify: inter-word;
  margin: 10px 0 0 0;
  color: white;

}

/* (E) EVENT "SPEECH BUBBLE CALLOUT" */
/* (E1) SHARED */
div.alt-event::before,
div.alt-event.right::before {
  content: "";
  border: 10px solid transparent;
  position: absolute;
}

/* (E2) FOR EVENTS ON THE LEFT */
div.alt-event::before {
  /* (E2-1) "MAGIC TRIANGLE" */
  border-left-color: $dark_custom;
  border-right: 0;

  /* (E2-2) POSITION TRIANGLE ON THE RIGHT */
  left: 100%;
  top: 20%;
}

/* (E3) FOR EVENTS ON THE RIGHT */
div.alt-event.right::before {
  /* (E3-1) "MAGIC TRIANGLE" */
  border-right-color: $dark_custom;
  border-left: 0;

  /* (E3-2) POSITION TRIANGLE ON THE LEFT */
  left: auto;
  right: 99.6%;
  top: 20%;
}

/* (F) EVENT CIRCLE ON TIMELINE */
/* (F1) SHARED */
div.alt-event::after,
div.alt-event.right::after {
  /* (F1-1) "MAGIC CIRCLE" */
  content: "";
  background: $cian_custom;
  border: 4px solid $purple_custom;
  width: 16px;
  height: 16px;
  border-radius: 50%;

  /* (F1-2) POSITION */
  position: absolute;
}

/* (F2) POSITION TO THE LEFT */
div.alt-event::after {
  top: 20%;
  left: 108.5%;
}

/* (F3) POSITION TO THE RIGHT */
div.alt-event.right::after {
  top: 20%;
  left: auto;
  right: 107.2%;
}</style>