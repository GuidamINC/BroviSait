<script setup lang="ts">
import BroviHeader from "@/components/Header.vue"
import BroviHero from "@/components/Hero.vue"
import BroviServices from "@/components/Services.vue"
import BroviAbout from "@/components/About.vue"
import fooooter from './components/footer.vue'
import contactts from './components/contacts.vue'
import workks from './components/works.vue'
</script>

<template>
  <BroviHeader></BroviHeader>
  <BroviHero></BroviHero>
  <BroviServices></BroviServices>
  <BroviAbout></BroviAbout>
  <workks />
  <contactts />
  <fooooter />
</template>

<style scoped></style>
