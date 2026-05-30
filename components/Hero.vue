<!-- components/Hero.vue -->
<template>
  <!-- Redujimos pt-32 a pt-12 y lg:pt-40 a lg:pt-20 para pegar el Hero a la Navbar -->
  <section id="inicio" class="relative pt-12 pb-20 lg:pt-20 lg:pb-28 overflow-hidden">
    <div class="max-w-6xl mx-auto px-4 flex flex-col lg:flex-row items-center justify-between gap-12 relative z-10">
      
      <!-- Columna de Texto -->
      <div class="w-full lg:w-1/2 text-center lg:text-left">
        <!-- Badge de Especialidad Técnica -->
        <div class="inline-flex items-center space-x-2 px-3 py-1.5 rounded-full bg-blue-100 dark:bg-blue-500/10 border border-blue-200 dark:border-blue-500/20 text-blue-700 dark:text-blue-400 text-xs font-semibold tracking-wide mb-6">
          <span class="relative flex h-2 w-2">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-blue-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2 w-2 bg-blue-500"></span>
          </span>
          <span>Ingeniería Full Stack & IA para Negocios B2B</span>
        </div>
        
        <!-- Título Principal -->
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-slate-900 dark:text-white tracking-tight leading-tight mb-6 transition-colors duration-300">
          Escala tu operación con <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-indigo-600 dark:from-blue-400 dark:to-indigo-400">software inteligente</span>
        </h1>
        
        <!-- Descripción -->
        <p class="text-lg text-slate-600 dark:text-slate-400 font-normal mb-8 max-w-xl mx-auto lg:mx-0 leading-relaxed transition-colors duration-300">
          Diseñamos plataformas web modernas, automatizamos procesos y desarrollamos soluciones basadas en datos para empresas que buscan crecer tecnológicamente.
        </p>
        
        <!-- Botones de Llamado a la Acción -->
        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start space-y-4 sm:space-y-0 sm:space-x-4">
          <a href="https://wa.me/tu_numero_aqui?text=Hola,%20me%20interesa%20escalar%20mi%20negocio%20con%20software." target="_blank" class="w-full sm:w-auto inline-flex items-center justify-center px-6 h-12 text-sm font-semibold text-white bg-blue-600 hover:bg-blue-500 rounded-xl transition-all shadow-lg shadow-blue-600/20">
            Agendar consulta técnica
          </a>
          <a href="#servicios" class="w-full sm:w-auto inline-flex items-center justify-center px-6 h-12 text-sm font-medium text-slate-700 dark:text-slate-300 hover:text-slate-900 dark:hover:text-white bg-white dark:bg-slate-900/60 hover:bg-slate-50 dark:hover:bg-slate-900 rounded-xl border border-slate-200 dark:border-slate-800 transition-all">
            Ver nuestras soluciones
          </a>
        </div>
      </div>

      <!-- Columna Visual (Mockup Minimalista SaaS) -->
      <!-- Se eliminó 'hidden sm:block', se ajustó el margen superior (mt-12) y se centró el contenido para móviles -->
      <div class="w-full lg:w-1/2 relative mt-12 lg:mt-0 flex justify-center">
        <div class="relative w-full max-w-lg bg-white/40 dark:bg-slate-900/40 backdrop-blur-xl border border-slate-200/50 dark:border-slate-800/50 rounded-2xl shadow-2xl p-6 overflow-hidden transition-colors duration-300">
          
          <!-- Cabecera de la ventana (estilo Mac/Terminal) -->
          <div class="flex items-center justify-between mb-6 border-b border-slate-200 dark:border-slate-800 pb-4">
            <div class="flex space-x-2">
              <div class="w-3 h-3 rounded-full bg-slate-300 dark:bg-slate-700"></div>
              <div class="w-3 h-3 rounded-full bg-slate-300 dark:bg-slate-700"></div>
              <div class="w-3 h-3 rounded-full bg-slate-300 dark:bg-slate-700"></div>
            </div>
            <div class="text-[10px] font-mono text-slate-400 dark:text-slate-500 uppercase tracking-widest">
              Analytics_Engine.ts
            </div>
          </div>
          
          <!-- Contenido interno simulando un panel de datos/IA -->
          <div class="space-y-4">
            <div class="flex gap-4">
              <!-- Tarjeta Métrica 1 -->
              <div class="h-24 w-1/3 bg-blue-50 dark:bg-blue-500/5 border border-blue-100 dark:border-blue-500/10 rounded-xl p-4 flex flex-col justify-end">
                <div class="h-2 w-1/2 bg-blue-200 dark:bg-blue-500/40 rounded mb-2"></div>
                <div class="h-6 w-3/4 bg-blue-400 dark:bg-blue-500/80 rounded"></div>
              </div>
              <!-- Gráfico de barras animado simulado -->
              <div class="h-24 w-2/3 bg-slate-50 dark:bg-slate-800/30 border border-slate-100 dark:border-slate-700/30 rounded-xl p-4 flex flex-col justify-between">
                <div class="h-2 w-1/4 bg-slate-200 dark:bg-slate-600 rounded"></div>
                <div class="flex items-end space-x-2 h-10">
                  <div class="w-full bg-indigo-200 dark:bg-indigo-500/40 rounded-t h-[40%]"></div>
                  <div class="w-full bg-indigo-300 dark:bg-indigo-500/60 rounded-t h-[60%]"></div>
                  <div class="w-full bg-indigo-400 dark:bg-indigo-500/80 rounded-t h-[80%]"></div>
                  <div class="w-full bg-blue-500 dark:bg-blue-500 rounded-t h-[100%] animate-pulse"></div>
                </div>
              </div>
            </div>
            <!-- Bloque de código/texto simulado -->
            <div class="h-32 w-full bg-slate-50 dark:bg-slate-800/30 border border-slate-100 dark:border-slate-700/30 rounded-xl p-4">
               <div class="h-3 w-1/3 bg-slate-200 dark:bg-slate-600 rounded mb-4"></div>
               <div class="space-y-3">
                 <div class="h-2 w-full bg-slate-200 dark:bg-slate-700/50 rounded"></div>
                 <div class="h-2 w-5/6 bg-slate-200 dark:bg-slate-700/50 rounded"></div>
                 <div class="h-2 w-4/6 bg-slate-200 dark:bg-slate-700/50 rounded"></div>
               </div>
            </div>
          </div>
          
          <!-- Notificación flotante de estado -->
          <div class="absolute -right-2 md:-right-6 top-1/2 transform -translate-y-1/2 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 shadow-xl rounded-xl p-3 flex items-center space-x-3 transition-colors duration-300">
             <div class="w-8 h-8 rounded-full bg-emerald-100 dark:bg-emerald-500/20 flex items-center justify-center">
               <svg class="w-4 h-4 text-emerald-600 dark:text-emerald-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
             </div>
             <div>
               <div class="text-xs font-bold text-slate-800 dark:text-slate-200">Sistema Activo</div>
               <div class="text-[10px] text-slate-500 dark:text-slate-400">Procesando datos...</div>
             </div>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>