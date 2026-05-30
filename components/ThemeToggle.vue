<!-- components/ThemeToggle.vue -->
<template>
  <button 
    @click="toggleTheme" 
    class="relative inline-flex items-center justify-center w-10 h-10 rounded-xl bg-white/50 dark:bg-slate-800/50 backdrop-blur-sm border border-slate-200 dark:border-slate-700 hover:bg-white dark:hover:bg-slate-800 transition-all duration-300 text-slate-600 dark:text-slate-300 focus:outline-none shadow-sm"
    aria-label="Cambiar tema"
  >
    <!-- Icono del Sol (Modo Claro) -->
    <svg 
      class="absolute w-5 h-5 transition-all duration-500 ease-in-out"
      :class="isDark ? 'opacity-0 rotate-90 scale-50' : 'opacity-100 rotate-0 scale-100'"
      fill="none" viewBox="0 0 24 24" stroke="currentColor"
    >
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
    </svg>

    <!-- Icono de la Luna (Modo Oscuro) -->
    <svg 
      class="absolute w-5 h-5 transition-all duration-500 ease-in-out"
      :class="isDark ? 'opacity-100 rotate-0 scale-100' : 'opacity-0 -rotate-90 scale-50'"
      fill="none" viewBox="0 0 24 24" stroke="currentColor"
    >
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z" />
    </svg>
  </button>
</template>

<script setup>
import { computed } from 'vue'
const colorMode = useColorMode()

// Verificamos si estamos en dark mode
const isDark = computed(() => colorMode.value === 'dark')

// Alternar entre temas
const toggleTheme = () => {
  colorMode.preference = isDark.value ? 'light' : 'dark'
}
</script>