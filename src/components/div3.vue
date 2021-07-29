<template>
  <div class="div3-container">
      <h1 class="pano-text">Pano?</h1>
        <div class="div3-subcontainer">
            <div class="div3-elements" v-for="el in div3Elemets" :key="el.id">
                <div class="img-container">
                    <img v-bind:src="el.pics">
                </div>
                <h1>{{el.h1}}</h1>
                <p>{{el.p}}</p>
            </div>
        </div>
  </div>
</template>

<script>
export default {
    name: 'div3',
    data() {
        return{
            div3Elemets: [
                {
                    id: 1,
                    pics: require('@/assets/mag-order.png'),
                    h1: 'Mag Order',
                    p: 'Order the food you love from our app'
                },
                {
                    id: 2,
                    pics: require('@/assets/pa-atud.png'),
                    h1: 'Pa Atud',
                    p: 'Safe and fast delivery'
                },
                {
                    id: 3,
                    pics: require('@/assets/tsibog-na.png'),
                    h1: 'Tsibog Na!',
                    p: 'Enjoy your food at home'
                }
            ]            
        }
    }
}
</script>

<style lang='scss'>
    $primaryColor: #2da81a;
    $secondaryColor: #949494;
    .div3-container {
        height: 100vh;
        width: 100%;
        position: relative;
            .pano-text {
                font-family: Arial, Helvetica, sans-serif;
                font-size: 2.5em;
                color: $primaryColor;
                margin: 3% 9% 5% 9%;
            }
            .div3-subcontainer {
                display: flex;
                    .div3-elements {
                        font-family: Arial, Helvetica, sans-serif;
                        height: auto;
                        margin: 0 auto;
                        h1 {
                            font-size: 2em;
                            text-align: center;
                            margin-bottom: 20px;
                            color: #222222;
                        }
                        p {
                            font-size: 1em;
                            text-align: center;
                            color: $secondaryColor;
                        }
                        img {
                            height: 300px;
                            width: 300px;
                        }
                    }
            }
    }

    @media screen and (max-width: 935px) {
        .div3-container {
            .div3-subcontainer {
                display: block;
                    .div3-elements {
                        .img-container {
                            width: 100%;
                            text-align: center;
                        }
                    }
            }
        }
}

</style>