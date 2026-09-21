<template>
    <section class = "about" id = "about">
        <div class = "container">
            <div class = "h-new">
                ОБ ОСНОВАТЕЛЕ
            </div>
            <div class = "container">
                <div class = "about-grid">
                    <div class = "about-img"></div>
                    <div class = "about-content">
                        <h1>Основатель</h1>
                        <p>Пироги — это настоящее воплощение домашнего уюта, 
                        тепла и кулинарных традиций. Свежая, только что 
                        извлеченная из печи выпечка с золотистой корочкой и 
                        богатой начинкой 
                        способна собрать за одним столом 
                        всю семью и украсить как будничный обед, 
                        так и праздничное застолье.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>

.about{
    padding: 120px 0;
    background-color: #1F272E;
}

.about-content h1{
    max-width: 480px;
    text-align: center;
    padding: 10px;
    line-height: 1.02;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif ;
    font-size: clamp(16px, 4vw, 32px);
    display: inline-flex;
    margin-bottom: 30px;
    color:#F1ECE9;
}

.about-content p{
    text-align: justify;
    font-family: Arial, Helvetica, sans-serif ;
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-left: 10px;
    padding-right: 10px;

    font-size: 14px;
    max-width: 480px;
    margin-bottom: 44px;
    color: #838383;
}

.container{
    max-width: 1240px;
    margin: 0 auto;
    padding: 0 32px;
}

.about-grid{
    display:flex;
    align-items:center;
    justify-content: space-between;
}

.about-img{
    height: 500px;
    display:block;
    overflow: hidden;
    position: relative;
    aspect-ratio: 4/5;
    background-color: #F1ECE9;
    border: 5px solid black;
    
    border-radius: 16px;
}

.about-content{

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
        color: #F1ECE9;
}

.h-new::before /*линия*/
{ 
        content: "";
        width: 40px;
        height: 1px;
        background-color: #F1ECE9;
}
@media (max-width: 800px){
    .about-img{
        max-height: 290px;
        max-width: 480px;
        margin: 0 auto;
    }
    .about{
        padding: 80px 0;
    }
    .about-grid{
        flex-direction: column;
    }
}
</style>