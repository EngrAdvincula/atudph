<template>
  <div class="favorite">
           <div class="text-fav">

           <h1>Ngamin na paborito mong <br><br> Pagkaon, Digdi samo! </h1>


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
       width: 100%;
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
  }

   @media screen and (max-width: 685px) {
      .favorite {
        .text-fav {
          padding: 0;
          top: 30%;
          h1 {
            font-size: 3em;
            text-align: center;
          }
        }
      }
   }
</style>
