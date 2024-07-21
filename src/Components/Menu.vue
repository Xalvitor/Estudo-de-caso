<script setup>
  import { ref } from "vue";
  let actualMenu = ref(0);
  let menu = [
    `Introdução`,
    `Praia do flamengo`,
    `Praia do buraquinho`,
  ]

  let changeMenu = (menuIndex) => actualMenu.value = menuIndex;

</script> 

<template>
  <div class="layout">
    <header>
      <a v-for='(item, index) in menu'
        :key="'menuitem' + index"
        @click = "changeMenu(index)"> 
        {{ item }}
      </a>
    </header>

    <main>

      <section v-show = 'actualMenu === 0'>
        <slot name="introduçao"></slot>
      </section>

      <section v-show = 'actualMenu === 1'>
        <slot name="pontoInteresse1"></slot>
      </section>

      <section v-show = 'actualMenu === 2'>
        <slot name="pontoInteresse2"></slot>
      </section>

    </main>

  </div>
</template>

<style scoped>

header{
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  margin: 0 10px;
}

</style>