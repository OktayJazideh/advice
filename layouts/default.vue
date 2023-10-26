<template>
    <div class="h-screen flex items-center justify-center">

        <div class="flex-col mx-10 rounded-xl px-5 w-66 h-80 max-sm:w-screen max-sm:mx-10 max-sm:h-80 container relative">
            <slot />
            <picture class="flex justify-center  max-sm:mt-30">
                <source media="(max-width:420px)" srcset="../assets/images/pattern-divider-mobile.svg" class=" w-50 mt-16 ">
                <img src="../assets/images/pattern-divider-desktop.svg" class=" w-50 mt-16">
            </picture>

            <div class="rounded-full w-12 h-12  flex justify-center items-center mx-auto mt-1 max-sm:mt-24 absolute ddd" ><img src="../assets/images/icon-dice.svg" alt="" class="w-5"></div>
        </div>
        
    </div>
</template>
<style>
    *{
        box-sizing: border-box;
        @font-face {
            font-family: mono;
            src: url("../assets/fonts/Manrope-VariableFont_wght.ttf");
        }
    }
    .container{
        background-color: hsl(217, 19%, 24%);
    }
    h1 {
        color: hsl(150, 100%, 66%);
        font-family: mono;
        font-weight: 600;
        
    }p{
        color: hsl(193, 38%, 86%);
        font-size: 28px;
        font-family: mono;
        font-weight: 800;
    }

    .ddd{
        top: 290px;
        left: 48%;
        background-color: hsl(150, 100%, 66%);
    }
    @media (max-width: 450px) {
        .ddd{
        top:200px ;
        left: 46%;
       
        }
 
    
    }

  @media (max-width: 640px) {
        .ddd{
        top:200px ;
        left: 46%;
        
        }
    
    
}
</style>
<script>
    
</script>