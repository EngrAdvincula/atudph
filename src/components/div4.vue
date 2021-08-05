<template>
  <div class="favorite">
           <div class="text-fav">
              <h1>Ngamin na paborito mong <br><br> Pagkaon, Digdi samo! </h1>
           </div>
                 <div class="div4-img-container">
          <img src="@/assets/fav.png" alt="Fav Image">
      </div>
  </div>
</template>

<script>
    export default {
          name: 'div4'
    }
</script>

<style lang="scss">
  $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  .favorite{
    background-color: $primaryColor;
    position: relative;
    height: 100vh;
    width: 100%;

    .text-fav {
       position: absolute;
       float: left;
       padding-top: 200px;
       padding-left: 125px;
    }
    h1 {
        line-height: 100%;
        font-size: 1.5 em;
        font-size: 60px;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: normal;
        color: #ffffff;
    }
    .div4-img-container {
                height: 100vh;
                width: 40%;
                position: relative;
                bottom: 0;
                img {
                    position: absolute;
                    bottom: 0;
                    width: 100%;
                    height: auto;
                    right: -140%;
                }
            }
  }
 

   @media screen and (max-width: 1251px) {
      .favorite {
        .text-fav {
          display: block;
          width: 100%;
          margin-left: auto;
          margin-right: auto;
          padding-top: 0;
          padding-left: 0;
          top: 60%;
          h1 {
            font-size: 3em;
            text-align: center;
          }
        }
        .div4-img-container {
          
                img {
                  height: 550px;
                  width: 400px;
                  top: -10%;
                  left: 70%;
                }
            }

      }
   }
 
  @media screen and (max-width: 630px) {

        .favorite {
          .text-fav {
            display: block;
            width: 100%;
            margin-left: auto;
            margin-right: auto;
            padding-top: 0;
            padding-left: 0;
            top: 60%;
            h1 {
              font-size: 2em;
              text-align: center;
            }
          }
          .div4-img-container {
            
                  img {
                    height: 400px;
                    width: 300px;
                    top: 7%;
                    left: 70%;
                  }
              }

        }

  }


@media screen and (max-width: 435px) {

    .favorite {
          .text-fav {
            display: block;
            width: 100%;
            margin-left: auto;
            margin-right: auto;
            padding-top: 0;
            padding-left: 0;
            top: 60%;
            h1 {
              font-size: 1.5em;
              text-align: center;
            }
          }
          .div4-img-container {
            
                  img {
                    height: 300px;
                    width: 250px;
                    top: 15%;
                    left: 30%;
                  }
              }

        }

}
 

</style>
