<script setup>

    defineProps({
        cotizacion:{
            type: Object,
            required: true
        }
    })

</script>

<template>
      <div class="contenedor-resultado">
        <h2>Cotización</h2>

        <div class="resultado">
          <img 
            :src="'https://cryptocompare.com//' + cotizacion.IMAGEURL" 
            alt="imagen cripto"
            >
          <div>
              <p>El precio es de: <span>{{ cotizacion.PRICE }}</span></p>
              <p>Precio mas alto del dia: <span>{{ cotizacion.HIGHDAY }}</span></p>
              <p>Precio mas bajo del dia: <span>{{ cotizacion.LOWDAY }}</span></p>
              <p>Variacion  ultimas 2 Horas: <span>{{ cotizacion.CHANGEPTC24HOUR }}%</span></p>
              <p>Ultima Actualizacion: <span>{{ cotizacion.LASTUPDATE }}</span></p>
          </div>
        </div>

      </div>
</template>

