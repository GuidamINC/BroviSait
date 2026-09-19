<template>
<section class = "services" id = "services">
    <div class = "container">
        <div class = "h-new">
            НАШИ УСЛУГИ
        </div>
        <div class="services-array">
            <div class = "service-item">
                <div class = "service-num">01</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
            <div class = "service-item">
                <div class = "service-num">02</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
            <div class = "service-item">
                <div class = "service-num">03</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
            <div class = "service-item">
                <div class = "service-num">04</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
            <div class = "service-item">
                <div class = "service-num">05</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
            <div class = "service-item">
                <div class = "service-num">06</div>
                <h3>Название услуги</h3>
                <div class = "service-desc">Описание услуги</div>
                <div class="service-price">Цена ₽</div>
            </div>
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

    .h-new /*сам текст*/
    {
        font-family: Arial, Helvetica, sans-serif;
        font-size: 16px;
        text-transform: uppercase;
        letter-spacing: 0.2em;
        display: inline-flex;
        align-items: center;
        gap: 12px;
        margin-bottom: 24px;
    }

    .h-new::before /*линия*/
    { 
        content: "";
        width: 40px;
        height: 1px;
        background-color: black;
    }

    .services-array{
        display:flex;
        flex-direction: column;
        border-top: 1px solid;
    }

    .service-item
    {
        display: grid;
        grid-template-columns: 60px 1fr 1.4fr auto;
        gap: 40px;
        align-items: center;
        padding: 40px 0;
        border-bottom: 1px solid ;
        transition: all .4s ease;
        cursor: pointer;
    }

    .service-num{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 20px;
        color: #7a7a7a;
    }

    .service-desc{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 18px;
        color: #7a7a7a;
    }

    .service-price{
        font-family: Arial, Helvetica, sans-serif;
        font-size: 24px;
        white-space-collapse: collapse;
        text-wrap-mode: nowrap;
    }

    .service-item h3{
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 400;
        letter-spacing: -0.01em;
        line-height: 1.15;
        font-size: 30px;
    }

    .service-item:hover{
        padding-left: 15px;
        padding-right: 15px;
        background-color: #ece8e4;
    }

    @media (max-width: 800px){
        .service-item{
            grid-template-columns: 40px 1fr;
            gap: 16px;
        }
        .service-desc{
            grid-column: 2;
        }
        .service-price{
            grid-column: 2;
            text-align: left;
        }
    }
</style>

