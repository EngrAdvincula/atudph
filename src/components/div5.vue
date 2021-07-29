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
    $primaryColor: #2da81a;
    $secondaryColor: #949494;
    .div5-container {
        display: flex;
        width: 100;
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
                width: 40%;
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
   
    @media screen and (max-width: 935px) {
        .div5-container {
            .div5-text-container {
                text-align: center;
                position: static;
                width: 100%;
                margin-top: 300px;
            }
            .div5-img-container {
                display: none;
            }
        }

    }
</style>