<template>
    <section class = "hero" id = "hero">
        
        <div class = "container">
            <div class = "hero-grid">
                <div class = "hero-content">
                    <h1>
                        Тута
                        брови смотреть можно
                    </h1>
                    <p> Пироги — это настоящее воплощение домашнего уюта, 
                        тепла и кулинарных традиций. Свежая, только что 
                        извлеченная из печи выпечка с золотистой корочкой и 
                        богатой начинкой 
                        способна собрать за одним столом 
                        всю семью и украсить как будничный обед, 
                        так и праздничное застолье.
                    </p>
                    <div class = "hero-actions">
                        <a class="button">
                            ЗАПИСАТЬСЯ
                        </a>
                        <a href = "#services" class ="services-hyperlink">
                            СМОТРЕТЬ УСЛУГИ
                        </a>
                    </div>
                </div>
                <div class = "hero-visuals">
                    <div class = "hero-img"></div>
                </div>
            </div>
        </div>
    </section>
</template>



<style scoped>


*{
    top: 0;
    left: 0;
    margin: 0;
    box-sizing: border-box;
}

.hero{
    position: relative;
    min-height: 70vh;
    padding: 160px 0 80px;
    align-items: center;
    display:flex;
    
}


.hero-img{
    display:block;
    overflow: hidden;
    position: relative;
    aspect-ratio: 4/5;
    background-color: black;
    border-radius: 32px;
}

.hero h1
{
    max-width: 480px;
    text-align: left;
    padding: 10px;
    line-height: 1.02;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif ;
    font-size: clamp(48px, 4vw, 64px);
    display: inline-flex;
    margin-bottom: 30px;
}

.hero p{
    text-align: justify;
    font-family: Arial, Helvetica, sans-serif ;
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-left: 10px;
    padding-right: 10px;

    font-size: 17px;
    max-width: 480px;
    margin-bottom: 44px;
    color: #838383;
}

.hero-grid{
    display: grid;
    grid-template-columns: 1.1fr 1fr;
    gap: 80px;
    align-items: center;
}

.hero-content{
    margin: 0;
    padding: 0;
}

.hero-visuals{
    margin: 0;
    padding: 0;
}



.hero-actions{
    display: flex;
    flex-wrap: wrap;
    padding: 10px;
    gap: 32px;
}

.button{
    font-family: Arial, Helvetica, sans-serif;
    display: inline-flex;
    align-items: center;
    gap: 12px;
    padding: 18px 38px;
    color: #F1ECE9;
    border-radius: 10px;
    font-size: 13px;
    letter-spacing: 0.12em;
    transition: all .35s ease;
    cursor: pointer;
    background-color: #E27D60;
}

.button:hover{
    background-color: #ce7258;
    color: #d4d0ce;
    border-radius: 20px;
}


.services-hyperlink{
    color:black;
    font-family: Arial, Helvetica, sans-serif;
    display: inline-flex;
    align-items: center;
    gap: 14px;
    text-decoration:underline;
    text-underline-offset: 5px;
    font-size: 13px;
    letter-spacing: 0.12em;
    transition: all .35s ease;
    cursor: pointer;
}

.services-hyperlink:hover{
    color: #bd6750;
}

@media (max-width: 1024px){
    .hero-img{
        max-width: 480px;
        margin: 0 auto;
    }

    .hero-grid{
        grid-template-columns: 1fr;
        gap: 60px;
    }

    .container{
        padding: 0 20px;
    }
}

</style>