<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Spotters Spain - Documentación / README</title>
  
  <!-- FontAwesome 6 Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800;900&family=Orbitron:wght@600;800;900&display=swap');

    :root {
      --bg-dark: #030611;
      --card-bg-start: rgba(12, 18, 45, 0.85);
      --card-bg-end: rgba(6, 9, 24, 0.92);
      --neon-cyan: #00d2ff;
      --neon-green: #00ffcc;
      --gold-yellow: #ffcc00;
      --accent-red: #ff0055;
      --chart-line: rgba(0, 210, 255, 0.12);
    }

    body {
      background-color: var(--bg-dark);
      font-family: 'Montserrat', sans-serif;
      color: #ffffff;
      min-height: 100vh;
      position: relative;
    }

    .nautical-chart-bg {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      background-color: var(--bg-dark);
      background-image: 
        radial-gradient(circle at 50% 20%, rgba(0, 210, 255, 0.08) 0%, transparent 60%),
        radial-gradient(circle at 80% 80%, rgba(0, 255, 204, 0.05) 0%, transparent 50%),
        linear-gradient(var(--chart-line) 1px, transparent 1px),
        linear-gradient(90deg, var(--chart-line) 1px, transparent 1px);
      background-size: 100% 100%, 100% 100%, 30px 30px, 30px 30px;
    }

    .card {
      background: linear-gradient(145deg, var(--card-bg-start), var(--card-bg-end));
      border: 1.5px solid var(--neon-cyan);
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 0 16px rgba(0, 210, 255, 0.15);
      backdrop-filter: blur(8px);
    }

    .orbitron {
      font-family: 'Orbitron', sans-serif;
    }
  </style>
</head>
<body class="p-4 md:p-8">

  <div class="nautical-chart-bg"></div>

  <main class="relative z-10 max-w-4xl mx-auto space-y-6">

    <!-- HERO / HEADER BANNER -->
    <header class="card border-yellow-400/50 shadow-yellow-500/20">
      <div class="flex flex-col md:flex-row items-center justify-between gap-4">
        <div class="flex items-center gap-4">
          <div class="w-16 h-16 rounded-2xl bg-black/60 border-2 border-cyan-400 flex items-center justify-center text-cyan-400 text-3xl shadow-lg shadow-cyan-500/30">
            <i class="fa-solid fa-plane-departure"></i>
          </div>
          <div>
            <h1 class="text-2xl md:text-3xl font-black text-white orbitron tracking-wide">Spotters Spain</h1>
            <p class="text-xs md:text-sm text-cyan-400 font-medium mt-1">
              Documentación Oficial del Proyecto (README)
            </p>
          </div>
        </div>
        <div class="flex items-center gap-2">
          <span class="px-3 py-1 bg-cyan-500/10 border border-cyan-400 text-cyan-400 text-xs font-bold rounded-lg orbitron">
            v1.0.1
          </span>
          <span class="px-3 py-1 bg-emerald-500/10 border border-emerald-400 text-emerald-400 text-xs font-bold rounded-lg orbitron">
            Operativo
          </span>
        </div>
      </div>
    </header>

    <!-- INTRODUCCIÓN -->
    <section class="card space-y-3">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-circle-info text-emerald-400"></i> Sobre la Aplicación
      </h2>
      <p class="text-sm text-slate-300 leading-relaxed">
        <strong class="text-white">Spotters Spain</strong> es una aplicación web y móvil (PWA/APK) diseñada por y para la comunidad de entusiastas de la aviación y la fotografía aeronáutica (<em>plane spotting</em>). Concentra herramientas tácticas de campo, telemetría meteorológica en tiempo real, mapas de puntos de avistamiento, seguimiento de flotas y avisos oficiales en una interfaz neón optimizada para uso en exteriores.
      </p>
    </section>

    <!-- CARACTERÍSTICAS PRINCIPALES -->
    <section class="card space-y-4">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-star text-yellow-400"></i> Funcionalidades Principales
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-3 text-xs md:text-sm">
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-crosshairs"></i> Radar & Tráfico en Tiempo Real
          </div>
          <p class="text-slate-300 text-xs">Seguimiento de aeronaves en vivo e integración con reproductores gráficos (Windy, Flightradar24, RadarBox).</p>
        </div>
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-map-location-dot"></i> Mapa Spotter LEBL
          </div>
          <p class="text-slate-300 text-xs">Miradores, accesos recomendados y coordenadas exactas para avistamiento en el Aeropuerto de Barcelona-El Prat.</p>
        </div>
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-cloud-sun-rain"></i> MeteoSpotter Live
          </div>
          <p class="text-slate-300 text-xs">Telemetría METAR/Open-Meteo, cálculo de pista activa por viento, ángulo solar (*Golden Hour*) y sugerencias ISO/Apertura.</p>
        </div>
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-book-bookmark"></i> Cuaderno de Campo (Log)
          </div>
          <p class="text-slate-300 text-xs">Registro local de avistamientos por matrícula, pista y fecha con exportación de datos a formato CSV.</p>
        </div>
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-building-shield"></i> Avisos EASA & FAA
          </div>
          <p class="text-slate-300 text-xs">Directivas de aeronavegabilidad y alertas operacionales traducidas automáticamente al español.</p>
        </div>
        <div class="p-3 bg-black/40 border border-cyan-500/20 rounded-xl space-y-1">
          <div class="font-bold text-emerald-400 flex items-center gap-2">
            <i class="fa-solid fa-gamepad"></i> Aero Neon Trivia
          </div>
          <p class="text-slate-300 text-xs">Módulo didáctico interactivo con preguntas sobre aviación comercial, cartografía y técnica fotográfica.</p>
        </div>
      </div>
    </section>

    <!-- ARQUITECTURA TÉCNICA -->
    <section class="card space-y-3">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-code text-cyan-400"></i> Arquitectura Técnica
      </h2>
      <ul class="list-disc pl-5 space-y-2 text-xs md:text-sm text-slate-300">
        <li><strong class="text-white">Frontend:</strong> HTML5 semántico, CSS3 customizado (animaciones neón, flexbox/grid), Tailwind CSS y FontAwesome 6.</li>
        <li><strong class="text-white">JavaScript:</strong> Vanilla JS (ES6+) asíncrono, renderizado en cliente, canvas 2D dinámico y síntesis de voz (Web Speech API).</li>
        <li><strong class="text-white">Motor Service Worker:</strong> Estrategia *Offline-First* con caché persistente y soporte PWA / APK.</li>
        <li><strong class="text-white">Almacenamiento Local:</strong> Datos de EASA/FAA y logs de usuario guardados en `localStorage` hasta un máximo de 10 días sin sobrecargar red.</li>
      </ul>
    </section>

    <!-- ESTRUCTURA DEL PROYECTO -->
    <section class="card space-y-3">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-folder-tree text-yellow-400"></i> Estructura del Sistema
      </h2>
      <div class="bg-black/60 p-4 rounded-xl border border-cyan-500/30 text-xs font-mono text-cyan-300 overflow-x-auto space-y-1">
        <div>├── index.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Pantalla principal, MeteoSpotter Live y Trivia</div>
        <div>├── p_spotting.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Mapa interactivo de miradores de aviación</div>
        <div>├── meteorologia.html &nbsp;&nbsp;&nbsp;&nbsp;# Sensores meteorológicos y cálculo de pista activa</div>
        <div>├── aerolineas.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Ficha técnica, flotas, libreas y Cuaderno Log (CSV)</div>
        <div>├── info_aeropu.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Información de pistas, ILS y frecuencias (LEBL / BCN)</div>
        <div>├── noticias.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Portal de noticias aeronáuticas traducidas</div>
        <div>├── alert.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Directivas de Aeronavegabilidad (EASA/FAA)</div>
        <div>├── enlaces.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Hub de la comunidad y perfiles recomendados</div>
        <div>├── colaboracion.html &nbsp;&nbsp;&nbsp;&nbsp; # Donaciones y soporte al proyecto (Bizum/PayPal/IBAN)</div>
        <div>└── acerca.html &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Términos legales, privacidad RGPD y sugerencias</div>
      </div>
    </section>

    <!-- PRIVACIDAD -->
    <section class="card space-y-3">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-shield-halved text-emerald-400"></i> Política de Privacidad & Marco Legal
      </h2>
      <p class="text-xs md:text-sm text-slate-300 leading-relaxed">
        Diseñado bajo la directriz de <strong>Privacy by Design</strong>. La aplicación no exige registro de usuario ni almacena datos personales en servidores externos. Las coordenadas GPS se procesan únicamente en la memoria RAM local del terminal del usuario para calcular distancias a aeropuertos. Cumple estrictamente con el <strong>RGPD (UE 2016/679)</strong> y la <strong>LOPDGDD 3/2018</strong>.
      </p>
    </section>

    <!-- EQUIPO -->
    <section class="card space-y-3">
      <h2 class="text-lg font-extrabold text-cyan-400 orbitron flex items-center gap-2 border-b border-cyan-500/20 pb-2">
        <i class="fa-solid fa-users text-yellow-400"></i> Desarrollo y Equipo
      </h2>
      <div class="text-xs md:text-sm text-slate-300 space-y-2">
        <p><strong class="text-white">Desarrollador Principal:</strong> Nelson Rosario García</p>
        <p><strong class="text-white">Contacto / Soporte:</strong> <a href="mailto:spottersspain@gmail.com" class="text-cyan-400 underline">spottersspain@gmail.com</a></p>
        <p><strong class="text-white">Equipo Tester y Colaboradores:</strong> Oscar Martínez Cortes, Toni Pozo Piñero, Alex Caro Martínez, Kevin González Leyva.</p>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="text-center text-xs text-slate-500 orbitron pt-4">
      Spotters Spain v1.0.1 · Todos los derechos reservados 2026
    </footer>

  </main>

</body>
</html>