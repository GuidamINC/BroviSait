<template>
<section class = "services" id = "services">
    <div class = "container">
        <div class = "h-new">
            НАШИ УСЛУГИ
        </div>
    </div>
</section>
</template>



<style scoped>
    .services{
        padding-top: 120px;
        padding-bottom: 120px;
        display: block;
        
    }
    .container{
        max-width: 1240px;
        margin: 0 auto;
        padding: 0 32px;

    }
    .h-new{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 16px;
        text-transform: uppercase;
        letter-spacing: 0.2em;
        display: inline-flex;
        align-items: center;
        gap: 12px;
        margin-bottom: 24px;
    }

    .h-new::before{
    content: "";
        width: 40px;
        height: 1px;
        background-color: black;
    }
</style>

