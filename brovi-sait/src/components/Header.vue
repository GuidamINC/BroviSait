<<template>
    <header class = "header-bg">
        <header class = "header-container">
            <div class = "title-text">Brovi</div>
            <a class = "s-a" href = "#hero">Главная</a>
            <a class = "s-a" href = "#services">Услуги</a>
            <a class = "s-a" href = "#hero">Об основателе</a>
            <a class = "s-a" href = "#hero">Наши работы</a>
            <a class = "s-a" href = "#hero">Контакты</a>
        </header>
    </header>
</template>

<script setup, lang="ts">

</script>

<style scoped>
.header-bg{
    background-color: #1F272E;

    top: 0;
    padding-left: 10px; 
    padding-right: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.85);

    
    box-sizing: border-box;
    position: sticky;
    
    z-index: 2;
}

.title-text
{
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 22px;
    font-style: italic;
    font-weight:400;
    color: #ffb587;
}

.s-a
{
    font-family: Arial, Helvetica, sans-serif;
    color: #F1ECE9;
    font-size: 16px;
    cursor: pointer;
    width:max-content;

    text-decoration: none;
    transition: all 0.3s ease-in-out;
}



.s-a:hover{
    color: #F96F52;
    text-decoration: underline;
    text-underline-offset: 5px;
    
}




.header-container{
    display: flex;
    justify-content: space-between;
    gap: 20px;
    align-items: center;
    margin: auto;
    
    max-width: 1200px;
    min-height: 55px;
    max-height: 70px; 
    width: 100%;
    
}

</style>