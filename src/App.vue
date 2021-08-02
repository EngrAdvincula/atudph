<template>
  <div id="app">
    <div id="nav">
      <h1 class="logo">
          <img src="@/assets/logo2.png" alt="Arud logo">
      </h1>
      <div class="burger">
          <div class="b1"></div>
          <div class="b2"></div>
          <div class="b3"></div>
      </div>
      <li>
        <ul href="#newsroom">
          Newsroom
        </ul>
        <ul href="#about">
          About
        </ul>
        <ul href="#contact">
          Contact
        </ul>
      </li>
    </div>
    <div2 />
    <div3 />
    <div4 />
    <div5 />
    <div6 />
    <div7 />
    <router-view/>
  </div>
</template>

<script>
import div2 from '@/components/div2.vue'
import div3 from '@/components/div3.vue'
import div4 from '@/components/div4.vue'
import div5 from '@/components/div5.vue'
import div6 from '@/components/div6.vue'
import div7 from '@/components/div7.vue'

  export default {
    components: {
      div2,
      div3, 
      div4,
      div5,
      div6,
      div7
    },
  }
</script>

<style lang="scss">
  $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  #nav {
    position: fixed;
    z-index: 999;
    width: 100%;
    height: 70px;
    background-color: $primaryColor;
    border-bottom: 1.5px rgb(75, 74, 74) solid;
      .burger {
        position: absolute;
        display: none;
        top: 16px;
        right: 2.5%;
        .b1{
          height: 6px;
          width: 40px;
          background-color: white;
          margin-bottom: 5px;
        }
        .b2{
          height: 6px;
          width: 40px;
          background-color: white;
          margin-bottom: 5px;
        }
        .b3 {
          height: 6px;
          width: 40px;
          background-color: white;
        }
      }
      .logo {
        img {
          position: absolute;
          top: 9px;
          left: 3%;
          height: 50px;
          width: 100px;
        }
      }
      li {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        color: white;
        font-size: 1em;
        display: flex;
        position: absolute;
        top: 27px;
        right: 5%;
          ul {
            margin-left: 40px;
              &:hover {
                color: rgb(46, 45, 45);
                cursor: pointer;
              }
          }
      }
  }

@media screen and (max-width: 480px) {
    #nav {
      position: static;
      .burger {
        display: block;
      }
      ul {
        display: none;
      }
    }
}



</style>