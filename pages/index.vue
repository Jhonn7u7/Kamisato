<template>
  <div>
  <hero/>
  <navbar/>
  <br>
  <br>
  <div class="container sw rounded p-4">
    <h2  class="text-center">¿Quienes somos?</h2>
    <p class="container  rounded p-4 col-6 text-center">Somos una página que intenta ayudar a los jugadores de juego Genshin Impact, nuestro principal objetivo es guiar al viajero a equipar a su personaje para que haga un daño muy alto</p>
  </div>
    <br>
    <br>
    <br>
    <div class="container sw rounded p-4">
    <h2 class="text-center" id="builds">Builds</h2>
    <b-row class="mt-4" cols="1" cols-md="3">
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center" >Ayaka <span><img src="~/assets/icon_1.png" alt="Ayaka" class="icon"></span></h5>
          <b-card-body>
            <p>una personaje cryo que utiliza espada ligera, actualmente es una de las mejores personajes cryo</p>
             <b-badge pill variant="dark" class="mx-1">DPS</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`buil/ayaka`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Ganyu <span><img src="~/assets/icon_2.png" alt="Ganyu" class="icon"></span></h5>
          <b-card-body>
            <p>una personaje cryo que utiliza el arco, actualmente es una de las mejores personajes cryo</p>
            <b-badge pill variant="dark" class="mx-1">DPS</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`buil/ganyu`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Bennet <span><img src="~/assets/icon_3.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Actualmente esta entre los mejores supports F2p que existen, este te cura y te aumenta el daño.</p>
            <b-badge pill variant="dark" class="mx-1">Support</b-badge><b-badge pill variant="dark" class="mx-1">Healer</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Keqing <span><img src="~/assets/icon_4.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>De mis personajes favoritos de electro, es muy rapida y su daño no estan elevado pero si te puede llegar a servir</p>
            <b-badge pill variant="dark" class="mx-1">DPS</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">xingqiu <span><img src="~/assets/icon_5.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Considerado el mejor support de hydro. con su elemental cura peo no al nivel de un healer.</p>
            <b-badge pill variant="dark" class="mx-1">Support</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Shogun Raiden<span><img src="~/assets/icon_6.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Puede funcionar de support o subdps, actualmente de las personas que recargan energia a otros personajes rapidamente</p>
            <b-badge pill variant="dark" class="mx-1">Support</b-badge><b-badge pill variant="dark" class="mx-1">SubDPS</b-badge><br><br>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </div>
  <!--  <div class="container sw rounded p-4">                            TALVEZ SE UTILIZE
    <h2 class="text-center" id="noticias">Noticiero Genshin</h2>
    <b-row class="mt-4" cols="1" cols-md="3">
      <b-col>
        <b-card no-body class="mt-4  h-75">
          <b-card-body>
            <p>¡La vista previa de la nueva versión 2.3 «Sombras de nieve y polvo» ya está disponible!</p>
            <a href="https://genshin.mihoyo.com/es/news/detail/17104" class="btn btn-primary">INFORMATE</a>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4 h-75">
          <b-card-body>
            <p>Detalles del Gachapón promocional de personaje 2 (Nuevo formato)</p>
            <a href="https://genshin.mihoyo.com/es/news/detail/17073" class="btn btn-primary  mt-4">INFORMATE</a>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Bennet <span><img src="~/assets/icon_3.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Ganyu es una personaje cryo que utiliza el arco, actualmente es una de las mejores personajes cryo</p>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Keqing <span><img src="~/assets/icon_4.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Ganyu es una personaje cryo que utiliza el arco, actualmente es una de las mejores personajes cryo</p>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">xingqiu <span><img src="~/assets/icon_5.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Ganyu es una personaje cryo que utiliza el arco, actualmente es una de las mejores personajes cryo</p>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body class="mt-4">
          <h5 class="text-center">Shogun Raiden<span><img src="~/assets/icon_6.png" alt="" class="icon"></span></h5>
          <b-card-body>
            <p>Ganyu es una personaje cryo que utiliza el arco, actualmente es una de las mejores personajes cryo</p>
            <b-button variant="primary" tag="nuxt-link" :to="`sales/${i}`"  size="sm">Saber mas</b-button>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </div> -->
  </div>
</template>

<style scoped>
 .sw{
   box-shadow: 0px 0px 12px 0px rgba(0,0,0,0.15);
 }
 .icon{
   width: 60px;
   height: 60px;
 }
</style>
<script>
export default {}
</script>
