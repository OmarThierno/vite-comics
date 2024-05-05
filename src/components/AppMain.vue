<script>
import ProductCard from './ProductCard.vue'
import { movies } from '../assets/data/dateUse';
  export default {
    components: {
      ProductCard,
    },
    data() {
      return{
        films: movies,
      }
    }
  }
</script>

<template>
  <main>
    <div class="hero"></div>

    <div class="container">
      <span class="current-series">CURRENT SERIES</span>
      <div class="row">
        <div v-for="curFilm in films" class="col">
          <ProductCard :cardImage="curFilm.thumb" :cardTitle="curFilm.series"/>
        </div>
      </div>
      <div class="btn-load-mode">
        <a href="">Load mode</a>
      </div>
    </div>
  </main>
  
</template>

<style lang='scss'>
  @use "../style/partials/mixin" as * ;
  @use "../style/partials/variables" as * ;

  main {
    background-color: black;

    .hero {
      min-height: 20vh;
      background-image: url('../assets/img/jumbotron.jpg');
      background-size: cover;
    }

    .container {
      padding: 30px 0;

      .current-series {
        color: white;
        background-color: $primary-color;
        display: inline-block;
        padding: 10px 20px;
        position: relative;
        bottom: 6vh;
      }

      .row {
        @include flex(row, space-between, stretch);
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 20px;

        .col {
          width: calc(100% / 6 - 50px / 6);
        }

      }
      .btn-load-mode {
        @include flex(row, center, center);

        a {
          color: white;
          display: inline-block;
          text-decoration: none;
          background-color: $primary-color;
          padding: 10px 40px;
          transition: background-color 0.15s, color 0.15s;

          &:hover {
            background-color: white;
            color: $primary-color;
          }
        }
      }
    }
  }
</style>