<template>
    <div class="malaki">
        <div class="sunod-malaki">
            <div class="maliit">
            <h1>Ano man an <br> muya mo,</h1>
            <h1 class="strong">Atud got you!</h1>
        </div>
        </div>
        <svg class="svg" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
             <path fill="#ffffff" fill-opacity="1" d="M0,64L60,58.7C120,53,240,43,360,48C480,53,600,75,720,106.7C840,139,960,181,1080,176C1200,171,1320,117,1380,90.7L1440,64L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
    </div>
    
</template>

<script>
export default {
    name: 'hero'
}
</script>

<style lang="scss">
    $swatch1:#2da81a;
    * {
        margin: 0;
        padding: 0;
    }
    .malaki {
        position: relative;
        width: 100%;
        height: 100vh;
        background-color:$swatch1;
            .sunod-malaki {
                height: 100vh;
                width: 100%;
            }
            .svg {
                position: absolute;
                bottom: 0;
            }
            .maliit {
                position: absolute;
                font-size: 1.5em;
                right: 15%;
                line-height: 350%;
                h1 {
                    color: white;
                    font-family: arial;
                    font-weight: 200;
                }
                .strong {
                    font-weight: bold;
                }
            }
    }
</style>