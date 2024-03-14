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

    <v-btn>
        Button
    </v-btn>



</template>
