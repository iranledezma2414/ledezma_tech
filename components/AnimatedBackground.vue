<!-- components/AnimatedBackground.vue -->
<template>
  <div class="fixed inset-0 overflow-hidden pointer-events-none -z-50 transition-colors duration-700 bg-slate-50 dark:bg-slate-950">
    
    <!-- Cuadrícula técnica (Grid) -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#80808012_1px,transparent_1px),linear-gradient(to_bottom,#80808012_1px,transparent_1px)] bg-[size:24px_24px] [mask-image:radial-gradient(ellipse_60%_50%_at_50%_0%,#000_70%,transparent_100%)]"></div>

    <!-- Orbe Azul (Flotando arriba a la izquierda) -->
    <div class="absolute top-[-10%] left-[-10%] w-[40rem] h-[40rem] rounded-full mix-blend-multiply dark:mix-blend-screen filter blur-[100px] opacity-70 dark:opacity-20 animate-blob bg-blue-300 dark:bg-blue-600"></div>
    
    <!-- Orbe Índigo (Flotando arriba a la derecha con retraso) -->
    <div class="absolute top-[10%] right-[-10%] w-[35rem] h-[35rem] rounded-full mix-blend-multiply dark:mix-blend-screen filter blur-[100px] opacity-70 dark:opacity-20 animate-blob animation-delay-2000 bg-indigo-300 dark:bg-indigo-600"></div>
    
    <!-- Orbe Púrpura (Flotando abajo al centro con más retraso) -->
    <div class="absolute -bottom-[20%] left-[20%] w-[45rem] h-[45rem] rounded-full mix-blend-multiply dark:mix-blend-screen filter blur-[100px] opacity-70 dark:opacity-20 animate-blob animation-delay-4000 bg-purple-300 dark:bg-purple-600"></div>
  
  </div>
</template>

<style scoped>
/* Animación suave de respiración y traslación */
@keyframes blob {
  0% { transform: translate(0px, 0px) scale(1); }
  33% { transform: translate(30px, -50px) scale(1.1); }
  66% { transform: translate(-20px, 20px) scale(0.9); }
  100% { transform: translate(0px, 0px) scale(1); }
}

.animate-blob {
  animation: blob 15s infinite alternate ease-in-out;
}

.animation-delay-2000 {
  animation-delay: 2s;
}

.animation-delay-4000 {
  animation-delay: 4s;
}
</style>