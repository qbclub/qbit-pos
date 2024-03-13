<script setup>

import data from '../data/store.json'
import logo from '../assets/logo.svg'



</script>
<template>
    <div>
        <img :src="logo" />
    </div>


    <div v-for="item, key in data">
        {{ key }}
    </div>

    <UAccordion color="gray" variant="solid" size="xl"
    class="container mx-auto"
        :items="[{ label: '1. What is Nuxt UI?', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }, { label: '2. Getting Started', content: 'Lorem ipsum dolor sit amet, consectet' }, { label: '3. Theming', content: 'et, consectetur adipiscing elit' }, { label: '4. Components', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit' }]">
      
        <template #item="{ item }">
            <p class="italic text-gray-900 dark:text-white ">
                {{ item.content }}
            </p>
        </template>

    </UAccordion>



</template>
