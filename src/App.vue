<script setup>

import Introdução from './Components/Introdução.vue'
import Menu from './Components/Menu.vue'
import PraiaDeBuraquinho from './Components/PraiaDeBuraquinho.vue';
import PraiaDoFlamengo from './Components/PraiaDoFlamengo.vue';

</script> 

<template>

        <Menu>

          <template #introduçao>

            <Introdução/>

          </template>

          <template #pontoInteresse1>

            <PraiaDoFlamengo/>

          </template>

          <template #pontoInteresse2>
            
            <PraiaDeBuraquinho/>

          </template>
          
        </Menu>

</template>
