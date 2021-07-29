<template>
  <div class="banner">
           <div class="text">
              <h1>Ano man an <br> muya mo,</h1>
              <h2>Atud got you!</h2>
              <a href="#" class="btn">Be Our Para Tinda <i class='fas fa-angle-right'></i></a>
              <a href="#" class="btn">Be Our Para Atud <i class='fas fa-angle-right'></i></a>
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
    height: 720px;
    width: 100%;

    .wave {
        position: absolute;
        bottom: -16%;
    }
    .text {
       max-width: 675px;
       float: right;
       width: 100%;
       padding-top: 135px;
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

</style>
















