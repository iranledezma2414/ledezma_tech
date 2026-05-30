<!-- app.vue -->
<template>
  <div class="min-h-screen font-sans text-slate-800 dark:text-slate-200 antialiased selection:bg-blue-500/30 transition-colors duration-300 flex flex-col">
    
    <AnimatedBackground />
    
    <!-- ENVOLVEMOS LA NAVBAR AQUÍ -->
    <ClientOnly>
      <Navbar />
    </ClientOnly>
    
    <main class="flex-grow">
      <Hero />
      
      <!-- Div temporal para simular scroll -->
      <div class="h-[500px] flex items-center justify-center border-t border-slate-200 dark:border-slate-800 mt-20">
        <p class="text-slate-400 dark:text-slate-600 text-sm">Más secciones irán aquí abajo...</p>
      </div>
    </main>
    
  </div>
</template>