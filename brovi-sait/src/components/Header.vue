
<script setup lang="ts">
import * as Globals from "@/globals" 
</script>


<<template>
    <nav class = "header-bg">
        <header class = "header-container">
            <a class = "title-text" href = "#hero">{{ Globals.brand_name }}</a>
            <div class = "nav-list">
                <a class = "s-a" href = "#services">{{ Globals.services_name }}</a>
                <a class = "s-a" href = "#about">{{ Globals.about_name }}</a>
                <a class = "s-a" href = "#hero">{{ Globals.gallery_name }}</a>
                <a class = "s-a" href = "#hero">{{ Globals.contacts_name }}</a>
            </div>
            <a class = "contacts-button" href= "#hero">{{Globals.contacts_button_text}}</a>
        </header>
    </nav>
</template>


<style scoped>
.header-bg{
    top:0;
    left:0;
    right:0;
    padding: 0 20px;
    width:100%;
    background-color: #1F272E;
    top: 0;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.85);

    
    box-sizing: border-box;
    position: fixed;
    
    z-index: 2;
}

.title-text
{
    font-family: 'Playfair Display', Georgia, serif;
    font-size: 22px;
    font-style: italic;
    font-weight:400;
    text-decoration: none;
    color: #ffb587;
}


.nav-list{
    padding-left: 5px;
    padding-right: 5px;
    display:flex;
    gap:100px;
    align-items: center;
    justify-content:space-between;
}

 .s-a
 {
    font-family: Arial, Helvetica, sans-serif;
    color: #F1ECE9;
    font-size: 16px;
    cursor: pointer;

    text-decoration: none;
    transition: all 0.3s ease-in-out;
}
.s-a:hover
{
    font-family: Arial, Helvetica, sans-serif;
    color: #F96F52;
    text-decoration: underline;
    text-underline-offset: 5px;
}

.contacts-button{
    font-family: Arial, Helvetica, sans-serif;
    text-decoration: none;
    background-color: #E27D60;
    font-size: 16px;
    cursor:pointer;
    padding: 10px 32px;
    color: #F1ECE9;
    border-radius: 10px;
    transition: all 0.2s ease-in-out;
}
.contacts-button:hover{
    background-color: #c96e55;
    color: #d4d0ce;
}


.header-container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: auto;
    
    max-width: 1200px;
    min-height: 55px;
    max-height: 70px; 
    width: 100%;
    
    
    
}

@media (max-width: 800px) {
   .nav-list{
    display:none
   }
}


</style>