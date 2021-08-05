<template>
  <div class="div5-container">
      <div class="div5-img-container">
          <img src="@/assets/para-atud.png" alt="Para-Atud Image">
      </div>
      <div class="div5-text-container">
                <h1>Maging Atud Paratinda</h1>
                <button class="paratinda-btn">Be a ParaTinda</button>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='scss'>

* {
     margin: 0;
     padding: 0;
}

    $primaryColor: #2da81a;
    $secondaryColor: #949494;
    .div5-container {
        display: flex;
        height: 100vh;
        position: relative;
            .div5-text-container {
                font-family: Arial, Helvetica, sans-serif;
                color: $primaryColor;
                position: absolute;
                left: 50%;
                top: 35%;
                    h1 {
                        font-size: 3.5em;
                    }
                    .paratinda-btn {
                        width: 200px;
                        height: 45px;
                        border-radius: 2px;
                        border: 1px solid $primaryColor;
                        background-color: white;
                        color: $primaryColor;
                        margin-top: 100px;
                        font-size: 1.4em;
                            &:hover {
                                color: white;
                                background-color: $primaryColor;
                                cursor: pointer;
                            }
                    }
            }
            .div5-img-container {
                height: 100vh;
                width: 55%;
                position: relative;
                bottom: 0;
                img {
                    position: absolute;
                    bottom: 0;
                    width: 100%;
                    height: auto;
                }
            }
    }
   

    @media screen and (max-width: 1591px) {
        .div5-container {
             .div5-img-container {
                       left: 1%;
                  }
        }
   }
   

   @media screen and (max-width: 1251px) {
             .div5-container {
                  width: 100%;
                  display: inline-block;
                  position: relative;
                  .div5-text-container {
                       position: absolute;
                         margin-left: auto;
                         margin-right: auto;
                         margin-top: 40px;
                         left: 0;
                         right: 0;
                         top: 50%;
                         text-align: center;
                  }
                       

               .div5-img-container {
                    width: 100%;
                    margin: 0;
                    padding: 0;
                         img {
                              position: absolute;
                              top: 4%;
                              width: 430px;
                              height: 400px;
                              margin-right: auto;
                              margin-left: auto;
                              left: 0;
                              right: 0;
                         }
                    }
                 
        }
   }


   @media screen and (max-width: 855px) {
        .div5-container {
             .div5-text-container {
                  margin-top: 100px;
                  line-height: 50px;
                  h1 {
                       line-height: 100%;
                  }
                 
             }
             
             
        }
   }

   @media screen and (max-width: 757px) {
        .div5-container {
             .div5-text-container {
                  margin-top: 100px;
                  h1 {
                       font-size: 3em;
                       line-height: 150%;
                  }
                  
             }
             
        }
   }

</style>