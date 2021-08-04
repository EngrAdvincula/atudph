<template>
<div class="container">
  <div class="black-overlay">
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
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        </div>
      </li>
      <li class="carousel__item"><img src="@/assets/img2.jpg" alt="">       
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img3.jpg" alt="">       
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img4.jpg" alt="">       
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img5.jpg" alt="">       
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
        </div></li>
      <li class="carousel__item"><img src="@/assets/img4.jpg" alt="">       
      <div class="centered">
        <h1>A New Food Delivery Service Launches in Bicol</h1>
        <h5>by Cyd Jae Abad | October 17,2020 | Newsroom | 0 Comments</h5>
        <h4>Bicol’s local Para TIndas shortcomings became a solution in giving job opportunities to different Para Atud. Hitting two birds with one stone, Atud will soon rise in Bicol to deliver whatever it is your heart wants.</h4>
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
    z-index: -10;
    

    ul {
      width: 100%;
      height: 700px;
      z-index: 1;
      background-color: black ;
    }

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
          width: 100%;
          height: 700px;
          object-fit: cover;
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
        border: 1px solid #fff;
        display: inline-block;
        border-radius: 50%;
        cursor: pointer;
        margin: 0 .125%;
        width: 9px;
        height: 9px;
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

.bottom-left {
  position: absolute;
  bottom: 8px;
  left: 16px;
}

.top-left {
  position: absolute;
  top: 8px;
  left: 16px;
}

.top-right {
  position: absolute;
  top: 8px;
  right: 16px;
}

.bottom-right {
  position: absolute;
  bottom: 8px;
  right: 16px;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
   h1 {
        line-height: 1.6;
        font-size: 1 em;
        font-size: 45px;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: 700;
        color: #ffffff;
        padding-bottom: 40px;
    }
    h5 {
        line-height: 1.6;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: normal;
        color: #ffffff;
        padding-bottom: 20px;
    }
    h4 {
        line-height: 1.6;
        font-family:  "Trebuchet MS", Helvetica, sans-serif;
        font-weight: normal;
        color: #ffffff;
    }
}

@include carousel(6);
</style>
