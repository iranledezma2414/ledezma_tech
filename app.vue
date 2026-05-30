<template>
  <div class="min-h-screen font-sans text-slate-800 dark:text-slate-200 antialiased selection:bg-blue-500/30 transition-colors duration-300 flex flex-col">
    
    <AnimatedBackground />
    
    <ClientOnly>
      <Navbar />
    </ClientOnly>
    
    <main class="flex-grow">
      <Hero />
      
      <Services />
      
      <div class="h-[200px] flex items-center justify-center border-t border-slate-200 dark:border-slate-800 mt-10">
        <p class="text-slate-400 dark:text-slate-600 text-sm">Más secciones irán aquí abajo...</p>
      </div>
    </main>
    
  </div>
</template>

<script setup>
</script>

<style>
/* ...tus estilos globales existentes... */
</style>