<script setup>
import { ref } from 'vue'
import IcOutlinePlus from './icons/IcOutlinePlus.vue'
import MaterialSymbolsDatabase from './icons/MaterialSymbolsDatabase.vue'
import MaterialSymbolsModelTraining from './icons/MaterialSymbolsModelTraining.vue'
import IcBaselineWidthFull from './icons/IcBaselineWidthFull.vue'

const linkStyles = ref(
  'ml-4 text-blue-500 decoration-none indent-2 hover:bg-blue-500 border-blue-500 border-1 hover:text-white duration-300 px-3 py-2 flex items-center bg-gray-50 rounded-md text-sm font-medium'
)
</script>
<template>
  <nav class="flex items-center bg-gray-50 p-4">
    <nuxt-link to="/" class="py-2 text-4xl font-bold decoration-none text-black hover:text-blue-500 mr-auto"><span class="text-blue-500">MAYD</span><span class="text-orange-500">Ai</span></nuxt-link>
    <nuxt-link :class="linkStyles" to="/load-model-data"><MaterialSymbolsDatabase />Load new data</nuxt-link>
    <nuxt-link :class="linkStyles" to="/train-model"><MaterialSymbolsModelTraining />Train model</nuxt-link>
    <nuxt-link :class="linkStyles" to="/input"><IcOutlinePlus />New combination</nuxt-link>
  </nav>
</template>
