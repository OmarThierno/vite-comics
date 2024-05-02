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
          <span>DIGITAL COMICS</span>
        </div>
        <div class="icon">
          <img src="../assets/img/buy-comics-merchandise.png" alt="">
          <span>DC ERCHANDISE</span>
        </div>
        <div class="icon">
          <img src="../assets/img/buy-comics-subscriptions.png" alt="">
          <span>SUBCRIVEPTION</span>
        </div>
        <div class="icon">
          <img class="position-icon" src="../assets/img/buy-comics-shop-locator.png" alt="">
          <span>COMIC SHOP LOCATOR</span>
        </div>
        <div class="icon">
          <img src="../assets/img/buy-dc-power-visa.svg" alt="">
          <span>DC POWER VISA</span>

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
      <div class="container">
        <div class="sign-up"><a href="">SIGN UP NOW!</a></div>
        <div class="social-icon">
          <span><a href="">FOLOW US</a></span>
          <ul>
            <li>
              <a href="">
                <img src="../assets/img/footer-youtube.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../assets/img/footer-youtube.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../assets/img/footer-youtube.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../assets/img/footer-pinterest.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../assets/img/footer-periscope.png" alt="">
              </a>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </footer>

</template>

<style lang='scss' scoped>
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

      .icon {
        display: flex;
        align-items: center;
        gap: 10px;
        color: white;

        img {
          width: 40px;
          &.position-icon {
            width: 25px;
          }
        }

        span {
          font-size: 0.6rem;
        }

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
        width: 30%;
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
        width: 70%;
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
    padding: 20px 0;
    position: relative;
    z-index: 2;
    background-color: #303030;
    @include flex(row, center, center);

    .sign-up {
      display: block;
      padding: 10px 20px;
      border: 2px solid $primary-color;
      color: white;
    }

    a {
      color: inherit;
      text-decoration: none;
    }
    .container {
      @include flex(row, space-between, center);

      .social-icon {
        @include flex(row, center, center);
        color: $primary-color;
    
        ul {
          list-style-type: none;
          @include flex(row, center, center);
          gap: 15px;
          margin-left: 15px;
    
          img {
            width: 30px
          }
        }
  
      }
    }


  }
}
</style>