<template>
    <div>
       <carousel >
            <carousel-slide v-for="slide in slides" :key="slide.id" class="carousel-slider">
                <img :src="slide.pics" :alt="slide">
            </carousel-slide>
        </carousel>
    </div>
</template>

<script>

import Carousel from '@/components/Carousel.vue';
import CarouselSlide from '@/components/CarouselSlide';


export default {
    name: 'div6',
    components: {
      Carousel : Carousel,
      CarouselSlide : CarouselSlide,
    },

    data(){
        return {
            slides: [
              {
                id: 1,
                pics: require('@/assets/logo3.png'),
                h1: '',
                p: ''
              },
              {
                id: 2,
                pics: require('@/assets/img2.jpg'),
                h1: '',
                p: ''
              },
              {
                id: 3,
                pics: require('@/assets/img3.jpg'),
                h1: '',
                p: ''
              },
              {
                id: 4,
                pics: require('@/assets/img4.jpg'),
                h1: '',
                p: ''
              },
              {
                id: 5,
                pics: require('@/assets/img5.jpg'),
                h1: '',
                p: ''
              } 
            ]
        }
    },
}
</script>

<style lang="scss">
 $primaryColor: #2da81a;
  * {
    margin: 0;
    padding: 0;
  }
  .carousel {
        position:relative;
        overflow: hidden;
        width:100%;
    }
    .btn {
        padding:5px 10px;
        background-color:rgba(0,0,0,0.5);
        border:1px solid transparent;
        margin:5px 10px;
        color:#FFF;
        height:50px;
        width:50px;
        position:absolute;
        margin-top:-25px;
        z-index:2;
    }
    .btn:hover {
        cursor: pointer;
    }
    .btn:focus{
        outline:none;
    }
    .btn-next {
        top:50%;
        right:0%;
        justify-content: flex-end;
    }
    .btn-prev {
        top:50%;
        left:0;
        justify-content: flex-end;
    }
    .carousel-slider {
        
        
    }
    .carousel-slider img {
        width:100%;
        height:100%;
    }
  
</style>