<template>
    <section class = "about" id = "about">
        <div class = "container">
            <div class = "h-new">
                ОБ ОСНОВАТЕЛЕ
            </div>
        </div>
    </section>
</template>


<style scoped>
.about{
    padding: 120px 0;
    background-color: #1F272E;
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
    .about{
        padding: 80px 0;
    }
}
</style>