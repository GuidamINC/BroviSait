<script setup>
const phone_number = "8-999-999-99-99"
const branch_address = "г.Чебоксары ул.БезымяннаяВысота дом Х3, 1 этаж"
const email = "ivanov_pupkin@gmail.ru" 

</script>

<template>
  <div class="page_footer"></div>
  <div class="main_footer">
    <div class="contacts_section">
      <div class="container">
        <div class="contacts">
        <div>{{phone_number}}</div>
        <div>{{branch_address}}</div>
        <div>{{email}}</div>
        </div>
      </div>
    </div>
    <footer class="main_footer">
      <div class="container">
        <div class="year">
          © 2026 Все права защищены.
        </div>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.main_footer{
  background-color: plum;
}
.container{
  display: flex;
  justify-content: center;
  height: 100px;
  width: 1280px;
  margin: auto;
}
</style>