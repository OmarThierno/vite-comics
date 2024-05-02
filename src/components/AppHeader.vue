<script>
  export default {
    data() {
      return {
        navList: [
          {
            title: 'CHARACTERS',
            visible: false,
          },
          {
            title: 'COMICS',
            visible: false,
          },
          {
            title: 'MOVIES',
            visible: false,
          },
          {
            title: 'TV',
            visible: false,
          },
          {
            title: 'GAMES',
            visible: false,
          },
          {
            title: 'COLLECTIBLES',
            visible: false,
          },
          {
            title: 'VIDEOS',
            visible: false,
          },
          {
            title: 'FANS',
            visible: false,
          },
          {
            title: 'NEWS',
            visible: false,
          },
          {
            title: 'SHOP',
            visible: false,
          },
        ],
      }
    }
  }
</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="navBar">
        <ul class="">
          <li @click="list.visible = !list.visible" v-for="list in navList" :class="{'active': list.visible}"><a href="">{{ list.title }}</a></li>
        </ul>
      </div>
    </div>
  </header>


  
</template>

<style lang='scss' scoped>
  @use "../style/partials/mixin" as * ;
  @use "../style/partials/variables" as * ;

  header {
    height: 80px;
    font-size: 0.7rem;
    display: flex;
    align-items: center;
    
    .container {
      display: flex;
      align-items: center;
      justify-content: space-between;

      .logo {
        width: 70px;
        display: flex;
        align-items: center;
  
        img {
          max-width: 100%;
        }
      }
      .navBar {
        ul{
          @include flex(row, center, center);
          list-style-type: none;
          gap: 10px;
          color: $primary-dark;
          line-height: 80px;
  
          li {
            
            a {
              color: inherit;
              text-decoration: none;
            }

            &:hover {
              color: $primary-color;
              border-bottom: 2px solid $primary-color;
            }
          }
        }
      }

    }

  }

  .active {
    border-bottom: 2px solid $primary-color;
  }
</style>