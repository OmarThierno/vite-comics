<script>
  export default {
    data() {
      return{
        
      }
    }
  }
</script>

<template>
  <main>
    <div class="container">
      <div> - - > Content goes here <--</div>
    </div>
  </main>
  
</template>

<style lang='scss'>
  @use "../style/partials/mixin" as * ;
  @use "../style/partials/variables" as * ;

  main {
    background-color: black;
    // debug
    @include flex(row, center, center);
    min-height: 200px;

    .container {

      div {
        color: white;
      }
    }
  }
</style>