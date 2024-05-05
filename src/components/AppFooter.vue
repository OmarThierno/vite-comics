<script>
import { dateImgFooter } from '../assets/data/dateUse';
export default {
  data() {
    return {
      images: dateImgFooter,
    }
  },
  methods: {
    getImgPath(img) {
      return new URL(`../assets/img/${img}`, import.meta.url).href;
    },
  }
}
</script>

<template>
  <footer>
    <section class="icon-section">
      <div class="container">
        <ul v-for="img in images" class="icon">
          <li>
            <img :src="getImgPath(img.pathRel)" :alt="img.title">
            <span>{{ img.title }}</span>
          </li>
        </ul>
      </div>
    </section>
    <section class="main-footer">
      <div class="container">
        <div class="footer-list">
          <div>
            <h4>DC COMICS</h4>
            <ul>
              <li><a href=""></a>Characters</li>
              <li><a href=""></a>Comics</li>
              <li><a href=""></a>Movies</li>
              <li><a href=""></a>Tv</li>
              <li><a href=""></a>Games</li>
              <li><a href=""></a>Video</li>
              <li><a href=""></a>New</li>
            </ul>

            <h4>SHOP</h4>
            <ul>
              <li><a href=""></a>Shop Dc</li>
              <li><a href=""></a>Shop Dc Collectibles</li>
            </ul>
          </div>

          <div>
            <h4>DC</h4>
            <ul>
              <li><a href=""></a>Terms Of Use</li>
              <li><a href=""></a>Privacy policy (New)</li>
              <li><a href=""></a>Add Chioce</li>
              <li><a href=""></a>Advertising</li>
              <li><a href=""></a>Jobs</li>
              <li><a href=""></a>Subscription</li>
              <li><a href=""></a>Talent Workshop</li>
              <li><a href=""></a>CPSC certificates</li>
              <li><a href=""></a>Ratings</li>
              <li><a href=""></a>Shop Help</li>
              <li><a href=""></a>Contact Us</li>
            </ul>
          </div>

          <div>
            <h4>SITES</h4>
            <ul>
              <li><a href=""></a>Dc</li>
              <li><a href=""></a>MAD Magazine</li>
              <li><a href=""></a>DC Kids</li>
              <li><a href=""></a>Dc Universe</li>
              <li><a href=""></a>DC Power Visa</li>
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
                <img src="../assets/img/footer-facebook.png" alt="">
              </a>
            </li>
            <li>
              <a href="">
                <img src="../assets/img/footer-twitter.png" alt="">
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

      ul.icon {
        list-style-type: none;
        display: flex;
        align-items: center;
        gap: 10px;
        color: white;

        li {
          @include flex(row, space-between, center);
          gap: 10px;
          img {
            width: 40px;
          }
  
          span {
            font-size: 0.6rem;
          }
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
          margin-bottom: 10px;
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