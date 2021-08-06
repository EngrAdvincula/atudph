<template>
    <div class="div7-container"> 
        <div class="div7-subcontainer">
            <img class="green-logo" src="@/assets/logo3.png" alt="atud logo green">
            <h3>Copyright 2020</h3>
            <div class="social-media-icons">
            <img src="@/assets/fb-logo.png" alt="fb logo">
            <img src="@/assets/insta-logo.png" alt="instagram logo">
        </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'div7'
}
</script>

<style lang="scss">
    .div7-container {
        position: relative;
        height: 90px;
        width: 100%;
        background-color: white;
        .div7-subcontainer {
            display: flex;
            width: 100%;
            .green-logo {
                position: absolute;
                top: 15px;
                left: 3%;
                width: 100px;
                height: 60px;
            }
            h3 {
                position: absolute;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                top: 30px;
                text-align: center;
                font-family: Arial, Helvetica, sans-serif;
                color: rgb(82, 80, 80);
            }
            .social-media-icons {
                display: flex;
                width: 50px;
                height: 30px;
                position: absolute;
                top: 20px;
                right: 10%;
                    img {
                        margin-left: 20px;
                    }
            }
        }
    }

@media screen and (max-width: 757px) {
    .div7-container{
        height: 65px;
        .div7-subcontainer{
            .green-logo{
                position: absolute;
                top: 0.1px;
                left: 4%;
                width: 80px;
                height: 50px;
            }
            h3{
               top: 23px;
               font-size: 1em;
              }

              .social-media-icons{
                right: 20%;
                width: 18px;
                height: 18px;
                top: 20px;

                img{
                    margin-left: 10px;
                }
               
              }
        }
    }
}
</style>