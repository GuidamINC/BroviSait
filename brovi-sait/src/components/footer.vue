<script setup>
import* as glb from "../globals.ts"
</script>

<template>
  <footer>
    <div class="container">
      <div class="footer-top">
        <div class="footer-brand">
          <a href="#" class="logo">{{ glb.brand_name }}</a>
          <p>Краткое описание салона</p>
        </div>
        <div class="footer-col">
          <h5>Навигация</h5>
          <ul>
            <li><a href="#about_author">Об основателе</a></li>
            <li><a href="#services">Услуги</a></li>
            <li><a href="#works">Наши работы</a></li>
            <li><a href="#contacts">Контакты</a></li>
          </ul>
        </div>
        <div class="footer-col contacts-col">
          <h5>Контакты</h5>
          <ul>
            <li><a :href="`tel:${glb.phone_number_raw}`">{{ glb.phone_number }}</a></li>
            <li><a :href="`mailto:${glb.email}`">{{ glb.email }}</a></li>
            <li>
              <div class="socials">
                <a href="instagram" aria-label="Instagram">
                  <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><rect x="2" y="2" width="20" height="20" rx="5" stroke="currentColor" stroke-width="1.5"/><circle cx="12" cy="12" r="4" stroke="currentColor" stroke-width="1.5"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor"/></svg>
                </a>
                <a href="telegram" aria-label="Telegram">
                  <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M22 2L11 13M22 2l-7 20-4-9-9-4 20-7z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/></svg>
                </a>
                <a href="whatsApp" aria-label="WhatsApp">
                  <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M21 11.5a8.4 8.4 0 01-12.3 7.5L3 21l2-5.4A8.4 8.4 0 1121 11.5z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/></svg>
                </a>
              </div>
            </li>
            <li>{{ glb.branch_address }}</li>
            <li>{{ glb.work_time }}</li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <div>© 2026 {{ glb.brand_name }}. Все права защищены.</div>
      </div>
    </div>
  </footer>
</template>


<style scoped>

.container {
  max-width: 1240px;
  margin: 0 auto;
  padding: 0 32px;
  
}

footer {
  color: #F1ECE9;
  padding: 80px 0 40px;
  background-color: #1F272E;
  font-family: Arial, Helvetica, sans-serif;
  
}

.footer-top {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 20px;
  padding-bottom: 20px;
  border-bottom: #F1ECE9 solid 1px;
  border-radius: 10px;
  flex-wrap: wrap;
}

.footer-col {
  flex: 1;
  padding: 24px;
  text-align: center;
}

.footer-brand {
  flex: 1;
  padding: 24px;
  text-align: center;
  
}

.footer-brand .logo {
  font-style: italic;
  display: block;
  color: #F1ECE9;
  font-size: 28px;
  font-weight: 700;
  margin-bottom: 20px;
  text-decoration: none;
  font-family: 'Playfair Display', Georgia, serif;
  text-shadow: 3px 3px 3px black;
}

.footer-brand p {
  font-size: 14px;
  line-height: 1.7;
  margin: 0 auto;
}

.footer-col h5 {
  font-size: 12px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  margin-top: 0;
  margin-bottom: 22px;
  font-weight: 500;
  font-family: 'Playfair Display', Georgia, serif;
}

.footer-col ul { 
  list-style: none; 
  display: flex; 
  flex-direction: column; 
  gap: 12px; 
  padding: 0;
  margin: 0; 
}

.footer-col li {
  font-size: 14px;
  line-height: 1.5;
  color: #838383; 
}

.footer-col a { 
  font-size: 14px;
  color: #838383; 
  text-decoration: none;
  transition: color .3s; 
}

.footer-col a:hover { 
  color: #F96F52;
}

.socials {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 15px;
  width: max-content;
  margin: 5px auto;
  padding: 0;
}

.socials a {
  display: flex;
  color: #838383;
  text-decoration: none;
  transition: transform 0.2s, opacity 0.2s;
}

.socials a:hover {
  opacity: 0.8;
  transform: scale(1.15);
}

.footer-bottom {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 0px;
  font-size: 13px;
  flex-wrap: wrap;
  gap: 20px;
  color: #838383;
  border-radius: 10px;
  height: 50px;
}
</style>