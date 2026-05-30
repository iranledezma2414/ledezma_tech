<template>
  <header class="sticky top-0 z-50 w-full bg-white/70 dark:bg-slate-950/80 backdrop-blur-lg border-b border-slate-200/50 dark:border-slate-800/50 transition-colors duration-300">
    <div class="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between relative">
      
      <div class="flex items-center space-x-2 z-50">
        <span class="text-xl font-black tracking-tight text-slate-900 dark:text-white transition-colors duration-300">Ledezma</span>
        <span class="text-xl font-light tracking-wide text-blue-600 dark:text-blue-400 transition-colors duration-300">Tech & Software</span>
      </div>

      <nav class="hidden md:flex space-x-8 text-sm font-medium text-slate-600 dark:text-slate-400">
        <a href="#inicio" class="hover:text-blue-600 dark:hover:text-white transition-colors duration-300">Inicio</a>
        <a href="#servicios" class="hover:text-blue-600 dark:hover:text-white transition-colors duration-300">Soluciones</a>
        <a href="#ventajas" class="hover:text-blue-600 dark:hover:text-white transition-colors duration-300">Tecnología</a>
      </nav>

      <div class="hidden md:flex items-center space-x-4 z-50">
        
        <button 
          @click="toggleTheme" 
          class="relative flex items-center justify-center w-10 h-10 rounded-xl bg-slate-100 dark:bg-slate-800 hover:bg-slate-200 dark:hover:bg-slate-700 transition-all duration-300 text-slate-600 dark:text-slate-300 focus:outline-none"
          aria-label="Alternar tema"
        >
          <svg class="absolute w-5 h-5 transition-all duration-500 ease-in-out" :class="isDark ? 'opacity-0 rotate-90 scale-50' : 'opacity-100 rotate-0 scale-100'" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
          </svg>
          <svg class="absolute w-5 h-5 transition-all duration-500 ease-in-out" :class="isDark ? 'opacity-100 rotate-0 scale-100' : 'opacity-0 -rotate-90 scale-50'" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
          </svg>
        </button>
        
        <a href="https://wa.me/tu_numero_aqui" target="_blank" class="inline-flex items-center justify-center px-4 h-9 text-xs font-semibold tracking-wide text-white bg-blue-600 hover:bg-blue-500 rounded-lg transition-all shadow-lg shadow-blue-600/20 dark:shadow-blue-600/10">
          Cotizar Proyecto
        </a>
      </div>

      <div class="flex items-center space-x-3 md:hidden z-50">
        
        <button @click="toggleTheme" class="relative flex items-center justify-center w-9 h-9 rounded-lg bg-slate-100 dark:bg-slate-800 text-slate-600 dark:text-slate-300 transition-all duration-300">
          <svg class="absolute w-4 h-4 transition-all duration-500" :class="isDark ? 'opacity-0 rotate-90 scale-50' : 'opacity-100 rotate-0 scale-100'" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" /></svg>
          <svg class="absolute w-4 h-4 transition-all duration-500" :class="isDark ? 'opacity-100 rotate-0 scale-100' : 'opacity-0 -rotate-90 scale-50'" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" /></svg>
        </button>

        <button @click="toggleMenu" class="p-2 text-slate-600 dark:text-slate-400 hover:text-slate-900 dark:hover:text-white transition-colors duration-300 focus:outline-none">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
    </div>

    <div 
      v-show="isMenuOpen" 
      class="absolute top-16 left-0 w-full bg-white dark:bg-slate-900 border-b border-slate-200 dark:border-slate-800 md:hidden flex flex-col px-6 py-6 shadow-2xl space-y-5 transition-colors duration-300"
    >
      <a href="#inicio" @click="closeMenu" class="text-slate-600 dark:text-slate-300 hover:text-blue-600 dark:hover:text-white font-medium text-base transition-colors duration-300">Inicio</a>
      <a href="#servicios" @click="closeMenu" class="text-slate-600 dark:text-slate-300 hover:text-blue-600 dark:hover:text-white font-medium text-base transition-colors duration-300">Soluciones</a>
      <a href="#ventajas" @click="closeMenu" class="text-slate-600 dark:text-slate-300 hover:text-blue-600 dark:hover:text-white font-medium text-base transition-colors duration-300">Tecnología</a>
      
      <div class="pt-4 border-t border-slate-200 dark:border-slate-800 transition-colors duration-300">
        <a href="https://wa.me/tu_numero_aqui" target="_blank" class="inline-flex items-center justify-center px-4 h-11 text-sm font-semibold tracking-wide text-white bg-blue-600 hover:bg-blue-500 rounded-lg w-full shadow-lg shadow-blue-600/20">
          Cotizar Proyecto
        </a>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
// Se asume que @nuxtjs/color-mode ya está instalado y configurado en nuxt.config.ts
const colorMode = useColorMode()

// Estado para el menú móvil
const isMenuOpen = ref(false)

// Computado para saber si estamos en modo oscuro
const isDark = computed(() => colorMode.value === 'dark')

// Funciones de control
const toggleTheme = () => {
  colorMode.preference = isDark.value ? 'light' : 'dark'
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>