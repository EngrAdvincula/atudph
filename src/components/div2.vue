<template>
  <div class="banner">
           <div class="img-container">
               <div class="atud-bike-container">
                    <img src="@/assets/atud-bike.png" alt="Atud Bike">
               </div>
               <div class="food-container">
                    <img src="@/assets/milk-tea.png" alt="Atud Milk Tea" class="milk-tea">
                    <img src="@/assets/coffee-cup.png" alt="Atud Coffee Cup" class="coffee-cup">
                    <img src="@/assets/burger.png" alt="Atud Burger" class="burger">
                    <img src="@/assets/chicken.png" alt="atud Chickern" class="chicken">
                    <img src="@/assets/fries.png" alt="atud fries" class="fries">
               </div>
           </div>
           <div class="text">
              <h1>Ano man an <br> muya mo,</h1>
              <h2>Atud got you!</h2>
               <div class="btn-container">
                    <a href="#" class="btn">Be Our Para Tinda <i class='fas fa-angle-right'></i></a>
                    <a href="#" class="btn">Be Our Para Atud <i class='fas fa-angle-right'></i></a>
               </div>     
           </div>

           <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320" class="wave">
           <path fill="#ffffff" fill-opacity="1" d="M0,64L60,58.7C120,53,240,43,360,48C480,53,600,75,720,106.7C840,139,960,181,1080,176C1200,171,1320,117,1380,90.7L1440,64L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>

  </div>
</template>

<script>
    export default {
          name: 'div2'
    }
</script>

<style lang="scss">
  $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  .banner{
    background-color: $primaryColor;
    position: relative;
    height: 100vh;
    width: 100%;

    .img-container {
         width: 100%;
         .atud-bike-container {
              position: absolute;
              top: 7%;
              left: 7%;
              img {
                   height: 700px;
                   width: 750px;
              }
         }
         .food-container {
               .milk-tea {
                    position: absolute;
                    right: 32%;
                    top: -8%;
               }
               .coffee-cup { 
                    height: 250px;
                    width: 230px;
                    position: absolute;
                    right: 4%;
                    top: 10%;
               }
               .burger {
                    position: absolute;
                    right: 10%;
                    top: 22%;
               }
               .chicken {
                    height: 400px;
                    width: 400px;
                    position: absolute;
                    right: 5%;
                    bottom: 20%;
               }
               .fries {
                    position: absolute;
                    bottom: 0;
                    right: 30%;
               }
         }
    }

    .wave {
        position: absolute;
        bottom: -16%;
    }
    .text {
       position: absolute;
       right: 20%;
       top: 20%;
          .btn-container {
               display: flex;
          }
           h1 {
               line-height: 150%;
               font-size: 1.5 em;
               font-size: 68px;
               font-family:  "Trebuchet MS", Helvetica, sans-serif;
               font-weight: normal;
               color: #ffffff;
          }
          h2 {
               line-height: 150%;
               font-size: 1.5 em;
               font-size: 75px;
               font-family: "Trebuchet MS", Helvetica, sans-serif;
               color: #ffffff;
          }

          .btn {
               position: relative;
               font-size: 16px;
               font-family: 'Poppins', sans-serif;
               font-weight: 700;
               background-color: #ffffff;
               color: $primaryColor;
               padding: 12px 0px;
               width: 100%;
               max-width: 190px;
               text-align: center;
               display: inline-block;
               text-transform: normal;
               text-decoration: none;
               border-radius: 25px;
               margin:1.2em 4em 1em 0;
               transition: 400ms;
               cursor: pointer;
               outline: none;
               overflow: hidden;
          }

          .btn:hover {
               background-color: #80b4d9;
               width: 190px;
               color: #ffffff;
               padding-right: 10px;
          }
          .btn .fas{
               position: absolute;
               top: 28%;
               margin-left: 10px;
               color: $primaryColor;
               transform: translateX(-50%);
               opacity: 0;
          }
          .btn:hover .fas {
               opacity: 1;
               transform: translateX(0);
          }
          .btn::before {
               content: '';
               position: absolute;
               left: 0;
               top: 0;
               width: 100%;
               height: 100%;
               background-color: rgba(0, 0, 0, .2);
               transform: scaleX(0);
               transition: 100ms ease-in-out transform;
          }
          .btn:active::before{
               transform: scaleX(1);
          }
          }
   
   }

   @media screen and (max-width: 1591px) {
        .banner {
             .img-container {
                  .atud-bike-container {
                       left: 1%;
                  }
                  .food-container {
                       .chicken{
                         height: 300px;
                         width: 300px;
                       }
                  }
             }
        }
   }

     @media screen and (max-width: 1425px) {
        .banner {
             .img-container {
                  .atud-bike-container {
                         img {
                              height: 500px;
                              width: 550px;
                         }
                  }
                  .food-container {
                       .chicken{
                         height: 300px;
                         width: 300px;
                       }
                  }
             }
        }
   }

   @media screen and (max-width: 1251px) {
        .banner {
             height: 1100px;
             .text {
                         margin-left: auto;
                         margin-right: auto;
                         left: 0;
                         right: 0;
                         text-align: center;

                         .btn-container {
                              width: 100%;
                              position: absolute;
                              .btn {
                                   margin-left: auto;
                                   margin-right: auto;
                                   left: 0;
                                   right: 0;
                                   text-align: center;
                              }
                         }
             }
             .img-container {
                  .atud-bike-container {
                         margin-left: auto;
                         margin-right: auto;
                         left: 0;
                         right: 0;
                         text-align: center;
                         top: -3%;

                         img {
                              height: 300px;
                              width: 350px;
                         }
                  }
                  .food-container {
                       .milk-tea {
                            left: 2%;
                            top: 20%;
                       }
                       .burger {
                            right: 2%;
                            top: 20%;
                       }
                       .coffee-cup {
                            display: none;
                       }

                       .fries {
                            bottom: 18%;
                            left: 2%;
                       }
                  }
             }
        }
   }

   @media screen and (max-width: 855px) {
        .banner {
             .text {
                  margin-top: 50px;
             }
             height: 100vh;
             .img-container {
                  .food-container {
                       .milk-tea {
                            left: 30%;
                            top: 65%;
                       }
                       .burger {
                            display: none;
                       }
                       .coffee-cup {
                            display: none;
                       }

                       .fries {
                            bottom: 0%;
                            left: 2%;
                       }
                       .chicken {
                            bottom: 0;
                            right: 2%;
                       }
                  }
             }
        }
   }

   @media screen and (max-width: 757px) {
        .banner {
             .text {
                  margin-top: 90px;
                  h1 {
                       font-size: 3em;
                  }
                  h2 {
                       font-size: 3em;
                  }
                  .btn-container {
                       display: block;
                       margin: 50px 0 0 0;
                         .btn {
                              margin: 0 10px;
                         }
                  }
             }
             height: 100vh;
             .img-container {
                  .food-container {
                       .milk-tea {
                           display: none;
                       }
                       .fries {
                            display: none;
                       }
                       .chicken {
                            display: none;
                       }
                  }
             }
        }
   }



</style>
















