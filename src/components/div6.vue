<template>
<div class="container">
  <div class="carousel">
    <input type="radio" id="carousel-1" name="carousel[]" checked>
    <input type="radio" id="carousel-2" name="carousel[]">
     <input type="radio" id="carousel-3" name="carousel[]">
    <input type="radio" id="carousel-4" name="carousel[]">
    <input type="radio" id="carousel-5" name="carousel[]">
    <input type="radio" id="carousel-6" name="carousel[]">
    <ul class="carousel__items">
      <li class="carousel__item"><img src="@/assets/img1.jpg" alt=""> 
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para Tindas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        <button class="readmore-btn">Read More</button>
        </div>
      </li>
      <li class="carousel__item"><img src="@/assets/img2.jpg" alt="">       
      <div class="centered">
        <h1>Nata dae ta na kaipuhan pang magluwas at magpa-deliver nasana kan pagkaon?</h1>
        <h5>by Cyd Jae Abad | March 15,2021 | Newsroom | 0 Comments</h5>
        <h4>Mag sasarong taon na bago kita saraduhan kang ekonomiya manungod sa Covid-19 Pandemic, tinawan kita ning pagpipilian, to stay safe in our homes or to take risk going outside.  Sa laog kang sarong taon na ini, nakapungaw ang mga panahong nagiiribahan kita sa mga...</h4>
        <button class="readmore-btn">Read More</button>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img3.jpg" alt="">       
      <div class="centered">
        <h1>San ba nagsimula ang milk tea at bakit hindi natin matigilan ito?</h1>
        <h5>by Cyd Jae Abad | March 3,2021 | Newsroom | 0 Comments</h5>
        <h4>Pagkatapos mong mabasa ito mapapasabi ka nalang na pa-Atud nga ng Milk tea. Makabagong kinahihiligan ng mga kabataan o kahit may edad man ang masarap na panghimagas na ito. Tila ba mayroong Milk Tea Craze na nangyayari, dahil samo’t saring mga franchise at iba’t ibang...</h4>
        <button class="readmore-btn">Read More</button>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img4.jpg" alt="">       
      <div class="centered">
        <h1>ANDITO NA ANG ATUD!</h1>
        <h5>by Cyd Jae Abad | February 23,2021 | Newsroom | 0 Comments</h5>
        <h4>February 22, 2021, 2.22.21, Atud officially made its soft-launch of their services.. The App is now downloadable and actively accepting orders. You can get the link through our Facebook and Instagram. The soft-launch started with a Blessing for the company and is...</h4>
        <button class="readmore-btn">Read More</button>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img5.jpg" alt="">       
      <div class="centered">
        <h1>Dios Mabalos 2020! A Year End Journey of Atud</h1>
        <h5>by Cyd Jae Abad | December 31,2020 | Newsroom | 0 Comments</h5>
        <h4>This 2020, we have witnessed how fast things could change as we welcome the new normal in our lives. Filipinos get by each day with resilience and with the help of all modern day heroes working on the front-lines. Above all the hardships and troubles we faced this year, let us look back at different milestones of Atud; despite the risk of Corona Virus and the other natural calamities, they do their job to help keep the world in motion.</h4>
        <button class="readmore-btn">Read More</button>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img6.jpg" alt="">       
      <div class="centered">
        <h1>On its way to 3rd District the Best Halo-Halo of Polangui!</h1>
        <h5>by Cyd Jae Abad | October 30,2020 | Newsroom | 0 Comments</h5>
        <h4>Formerly known as Tiya Benny’s Halo-halo since the 1960’s, this was actually owned by the great-grandmother Modesta “Muding” Samper and was then continued by her daughter Virgina “Benny”Achas who became well-known during the 1970’s — Tess Achas Halo-halo of Polangui, Albay continues to grow as new generations take over but the way their halo-halo is prepared remains and
tastes as good as before.</h4>
        <button class="readmore-btn">Read More</button>
        </div></li>
    </ul>
     <div class="carousel__prev">
      <label for="carousel-1"></label>
      <label for="carousel-2"></label>
      <label for="carousel-3"></label>
      <label for="carousel-4"></label>
      <label for="carousel-5"></label>
      <label for="carousel-6"></label>
     </div>
     <div class="carousel__next">
       <label for="carousel-1"></label>
       <label for="carousel-2"></label>
       <label for="carousel-3"></label>
       <label for="carousel-4"></label>
       <label for="carousel-5"></label>
       <label for="carousel-6"></label>
     </div>
     <div class="carousel__nav">
       <label for="carousel-1"></label>
       <label for="carousel-2"></label>
       <label for="carousel-3"></label>
       <label for="carousel-4"></label>
       <label for="carousel-5"></label>
       <label for="carousel-6"></label>
     </div>
   </div>
 </div>
</template>

<script>
    export default {
          name: 'divs6'
    }
</script>

<style lang="scss">
  $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  
%animation-default {
  opacity: 1 !important;
  z-index: 3;
  
}

@mixin carousel($items, $animation: 'default') {
  .carousel {
    width: 100%;
    position: relative;
    overflow: hidden;
    background-size: cover;

    > input[type="radio"] {
      position: absolute;
      left: 0;
      opacity: 0;
      top: 0;

      &:checked {
        ~ .carousel__items .carousel__item,
        ~ .carousel__prev > label,
        ~ .carousel__next > label {
          opacity: 0;
        }
      }

      @for $i from 1 through $items {
        &:nth-child(#{$i}) {
          &:checked {
            ~ .carousel__items .carousel__item {
              @if $animation == 'default' {
                &:nth-child(#{$i}) {
                  opacity: 1;
                }
              }
            }

            ~ .carousel__prev {
              > label {
                @if $i == 1 {
                  &:nth-child(#{$items}) {
                    @extend %animation-default;
                  }
                } @else if $i == $items {
                  &:nth-child(#{$items - 1}) {
                    @extend %animation-default;
                  }
                } @else {
                  &:nth-child(#{$i - 1}) {
                    @extend %animation-default;
                  }
                }
              }
            }

            ~ .carousel__next {
              > label {
                @if $i == $items {
                  &:nth-child(1) {
                    @extend %animation-default;
                  }
                } @else {
                  &:nth-child(#{$i + 1}) {
                    @extend %animation-default;
                  }
                }
              }
            }

            ~ .carousel__nav {
              > label {
                &:nth-child(#{$i}) {
                  background: #ccc;
                  cursor: default;
                  pointer-events: none;
                }
              }
            }
          }
        }
      }
    }

    &__items {
      margin: 0;
      padding: 0;
      list-style-type: none;
      width: 100%;
      height: 650px;
      position: relative;
    }

    &__item {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      transition: opacity 2s;
      -webkit-transition: opacity 2s;

      img {
        height: 700px;
        object-fit: cover;
        width: 100%;
        vertical-align: middle;
      }
    }

    &__prev,
    &__next {
      > label {
        cursor: pointer;
        display: block;
        width: 40px;
        height: 40px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        -webkit-transform: translateY(-50%);
        transition: all .3s ease;
        -webkit-transition: all .3s ease;
        opacity: 0;
        z-index: 2;

        &:hover,
        &:focus {
          opacity: .5 !important;
        }

        &:before,
        &:after {
          content: "";
          position: absolute;
          width: inherit;
          height: inherit;
        }

        &:before {
          background: linear-gradient(to top, #fff 0%, #fff 10%, rgba(51, 51, 51, 0) 10%),
                      linear-gradient(to left, #fff 0%, #fff 10%, rgba(51, 51, 51, 0) 10%);
          width: 60%;
          height: 60%;
          top: 20%;
        }
      }
    }

    &__prev {
      > label {
        left: 2%;

        &:before {
          left: 35%;
          top: 20%;
          transform: rotate(135deg);
          -webkit-transform: rotate(135deg);
        }
      }
    }

    &__next {
      > label {
        right: 2%;

        &:before {
          left: 10%;
          transform: rotate(315deg);
          -webkit-transform: rotate(315deg);
        }
      }
    }

    &__nav {
      position: absolute;
      bottom: 3%;
      left: 0;
      text-align: center;
      width: 100%;
      z-index: 3;

      > label {
        background: grey;
        opacity: 1;
        display: inline-block;
        border-radius: 50%;
        cursor: pointer;
        margin: 0 .350%;
        width: 8px;
        height: 8px;
      }
    }
  }
}

*,
*:before,
*:after {
  box-sizing: border-box;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
}

body {
  background: #fcfcfc;
  margin: 0;
}

.container {
  position: relative;
  object-fit: cover;
  width: 100%;
  margin: auto;
  text-align: center;


.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  
   h1 {
        line-height: 1.6;
        font-size: 1 em;
        font-size: 45px;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: 700;
        color: #ffffff;
        padding-bottom: 40px;
        animation-name: bottomFadeOut;
        animation-delay: 10s;
        animation-duration: 9s;
        
    }
    h5 {
        line-height: 1.6;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: lighter;
        color: #ffffff;
        padding-bottom: 20px;
        animation-name: bottomFadeOut;
        animation-delay: 10s;
        animation-duration: 9s;
    }
    h4 {
        letter-spacing: 0.2px;
        line-height: 1.6;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: lighter;
        color: #ffffff;
        animation-name: bottomFadeOut;
        animation-delay: 10s;
        animation-duration: 9s;
    }

   .readmore-btn {
        width: 130px;
        height: 40px;
        border-radius: 3px;
        border: 1px solid white;
        background-color: transparent;
        color: white;
        margin-top: 30px;
        font-size: 1.1em;
              &:hover {
                color: white;
                background-color: grey;
                cursor: pointer;
              }
        }
}
}
@media screen and (max-width: 757px) {
        .carousel {

          img{
            height: 700px;
            object-fit: cover;
          }
             .centered {

            
                  h1 {
                       font-size: 1.1em;
                       line-height: 1.6;
                  }
                  h5 {
                       line-height: 1.6;
                       font-size: 0.7em;
                  }
                  h4 {
                       line-height: 1.7;
                       font-size: 0.8em;
                  }
      
             }
        }
      }

@include carousel(6);
</style>
