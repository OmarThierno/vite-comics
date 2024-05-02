<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<template>
  <footer>
    <section class="icon-section">
      <div class="container">
        <div class="icon">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="">

        </div>
        <div class="icon">
          <img src="../assets/img/buy-comics-merchandise.png" alt="">

        </div>
        <div class="icon">
          <img src="../assets/img/buy-comics-subscriptions.png" alt="">

        </div>
        <div class="icon">
          <img src="../assets/img/buy-comics-shop-locator.png" alt="">

        </div>
        <div class="icon">
          <img src="../assets/img/buy-dc-power-visa.svg" alt="">

        </div>
      </div>
    </section>
    <section class="main-footer">
      <div class="container">
        <div class="footer-list">
          <div>
            <h4>DC COMICS</h4>
            <ul>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
            </ul>

            <h4>SHOP</h4>
            <ul>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
            </ul>
          </div>

          <div>
            <h4>DC</h4>
            <ul>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
            </ul>
          </div>

          <div>
            <h4>SITES</h4>
            <ul>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Characters</li>
            </ul>
          </div>
        </div>
        <div class="logo-footer">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>

      </div>
    </section>
    <section class="sign-up-section">
      <div class="container">ashashc</div>
    </section>
  </footer>

</template>

<style lang='scss'>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

footer {  
  .icon-section {
    background-color: $primary-color;
    padding: 20px 0;
    // min-height: 100px;

    .container {
      // height: 100%;
      @include flex(row, space-around, center);

      img {
        width: 40px;
      }
    }
  }

  .main-footer {
    min-height: 200px;
    padding: 30px 0;
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;

    .container {
      display: flex;
  
      .footer-list {
        width: 40%;
        display: flex;
        justify-content: space-between;
  
        h4 {
          font-size: 1rem;
          color: white;
        }
    
        ul {
          list-style-type: none;
          color: grey;
          font-size: 0.7rem;
        }
      }
  
      .logo-footer {
        text-align: center;
        width: 60%;
        position: relative;
        img {
          display: block;
          width: 300px;
          position: absolute;
          top: -60px;
          right: 0;
        }
      }

      
    }
    
  }
  .sign-up-section {
    z-index: 2;
    background-color: #303030;
    min-height: 100px;
    text-align: center;
  }
}
</style>