<script setup>
useSeoMeta({
  title: 'Кубит:автоматизация торговли',
  ogTitle: 'Кубит:автоматизация торговли',
  description: 'Кубит:автоматизация торговли, г. Глазов - комплексные решения для автоматизации торговли: онлайн-кассы, фискальные регистраторы, POS-системы, весы и другое оборудование для соответствия 54-ФЗ и ЕГАИС',
  ogDescription: 'Кубит:автоматизация торговли, г. Глазов - комплексные решения для автоматизации торговли: онлайн-кассы, фискальные регистраторы, POS-системы, весы и другое оборудование для соответствия 54-ФЗ и ЕГАИС',
  ogImage: 'https://qbit-torgob.ru/_nuxt/logo.DtTY1VtV.png',
  twitterCard: 'summary_large_image',
})

// {
//       rel: 'preconnect',
//       href: 'https://fonts.googleapis.com'
//     },
useHead({
  link: [
    {
      rel: 'icon',
      href: '/favicon.ico',
      sizes: '32x32'
    },
    {
      rel: 'icon',
      href: '/icon.svg"',
      type:"image/svg+xml"
    },
    {
      rel: 'apple-touch-icon',
      href: '/apple-touch-icon.png',
     
    },
    {
      rel: 'manifest',
      href: '/site.webmanifest',
     
    }
 
  ]
})


</script>

<template>

  <v-app>
    <v-container>
      <NuxtPage />
    </v-container>

  </v-app>

</template>
