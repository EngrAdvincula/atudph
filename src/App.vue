<template>
  <div id="app">
    <div id="nav">
      <h1 class="logo">
          Atud
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
        <ul href="contact">
          Contact
        </ul>
      </li>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
  $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  #nav {
    width: 100%;
    height: 70px;
    background-color: $primaryColor;
    position: relative;
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
        color: white;
        font-family: Arial, Helvetica, sans-serif;
        position: absolute;
        top: 15px;
        left: 3%;
      }
      li {
        font-family: Arial, Helvetica, sans-serif;
        font-weight: bold;
        color: white;
        font-size: 1.25em;
        display: flex;
        position: absolute;
        top: 20px;
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
      .burger {
        display: block;
      }
      ul {
        display: none;

      }
    }
}
</style>
