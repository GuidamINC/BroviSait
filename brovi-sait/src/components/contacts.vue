<script setup>
import* as glb from "../globals.ts"
</script>

<template>
<section class="booking" id="contacts">
  <div class="container">
    <div class="booking-wrap">
      <div class="booking-info">
        <div class="section-tag">Контакты</div>
        <ul class="contact-list">
          <li>
            <div class="contact-icon">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6 19.79 19.79 0 01-3.07-8.67A2 2 0 014.11 2h3a2 2 0 012 1.72c.13.96.37 1.9.72 2.81a2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.91.35 1.85.59 2.81.72A2 2 0 0122 16.92z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </div>
            <div>
              <span class="c-label">Телефон</span>
              <div class="c-value">{{glb.phone_number}}</div>
            </div>
          </li>
          <li>
            <div class="contact-icon">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" stroke="currentColor" stroke-width="1.5"/><path d="M22 6l-10 7L2 6" stroke="currentColor" stroke-width="1.5"/></svg>
            </div>
            <div>
              <span class="c-label">Email</span>
              <div class="c-value">{{glb.email}}</div>
            </div>
          </li>
          <li>
            <div class="contact-icon">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z" stroke="currentColor" stroke-width="1.5"/><circle cx="12" cy="10" r="3" stroke="currentColor" stroke-width="1.5"/></svg>
            </div>
            <div>
              <span class="c-label">Адрес</span>
              <div class="c-value">{{glb.branch_address }}</div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>
</template>

<style scoped>
.booking {
    background: #F1ECE9;
    
}
section { padding: 120px 0; }

.section-tag 
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

.section-tag::before 
{ 
    content: "";
    width: 40px;
    height: 1px;
    background-color: black;
}
.container {
  max-width: 1240px;
  margin: 0 auto;
  padding: 0 32px;
}
.booking-warp {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 20px;
    padding-bottom: 20px;
}
.contact-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    font-family: Arial, Helvetica, sans-serif;
    gap: 22px;
}
.contact-list li {
    display: flex;
    align-items: flex-start;
    gap: 18px;
    font-size: 15px;
}
.contact-icon {
    width: 42px; height: 42px;
    border-radius: 50%;
    border: 1px solid var(--line);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    color: #F96F52;
}
.contact-list .c-label {
    font-size: 12px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-top: 0;
    margin-bottom: 22px;
    font-weight: 500;
    font-family: 'Playfair Display', Georgia, serif;
}
.contact-list .c-value { 
    font-size: 14px;
    line-height: 1.5;
    
}

</style>