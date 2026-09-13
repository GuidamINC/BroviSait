<template>
    <section class = "hero-section" id = "hero">
        <picture>
            <img class = "hero-img" src = "@/assets/hero.webp" loading="lazy"></img>
        </picture>
    </section>
</template>



<style scoped>
*{
    top: 0;
    left: 0;
}
.hero-section{
    position: relative;
    
    width: 100%;
    height: 600px;
    

}
.hero-img{
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover; 
    object-position: 50% 62%;
    filter: brightness(0.75)


}

</style>