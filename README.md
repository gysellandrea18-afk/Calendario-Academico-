#Calendario Academico 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Calendario Académico 2026 – Encuentros y Entregas | UTS</title>
  
  <link href="https://cdn.jsdelivr.net/npm/fullcalendar@6.1.15/index.global.min.css" rel="stylesheet" />
  
  <style>
    :root {
      --bg: #0f172a;
      --card: #1e293b;
      --text: #e2e8f0;
      --accent: #3b82f6;
      --border: #334155;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
      padding: 20px;
    }

    header {
      max-width: 1100px;
      margin: 0 auto 24px;
    }

    h1 {
      font-size: 1.6rem;
      font-weight: 700;
      margin-bottom: 4px;
    }

    .subtitle {
      color: #94a3b8;
      font-size: 0.95rem;
      margin-bottom: 16px;
    }

    .legend {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      font-size: 0.9rem;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .dot {
      width: 14px;
      height: 14px;
      border-radius: 4px;
    }

    .dot.encuentro { background: #3b82f6; }
    .dot.entrega   { background: #22c55e; }

    #calendar {
      max-width: 1100px;
      margin: 0 auto;
      background: var(--card);
      border-radius: 12px;
      padding: 16px;
      box-shadow: 0 4px 24px rgba(0,0,0,0.4);
    }

    .fc {
      --fc-border-color: var(--border);
      --fc-page-bg-color: transparent;
      --fc-neutral-bg-color: #1e293b;
      --fc-list-event-hover-bg-color: #334155;
      --fc-today-bg-color: rgba(59, 130, 246, 0.12);
    }

    .fc .fc-toolbar-title {
      font-size: 1.25rem;
      color: var(--text);
    }

    .fc .fc-button {
      background: #334155 !important;
      border: none !important;
      text-transform: capitalize;
      font-size: 0.85rem;
    }

    .fc .fc-button:hover {
      background: #475569 !important;
    }

    .fc .fc-button-primary:not(:disabled).fc-button-active {
      background: var(--accent) !important;
    }

    .fc-theme-standard td, .fc-theme-standard th {
      border-color: var(--border);
    }

    .fc .fc-col-header-cell-cushion,
    .fc .fc-daygrid-day-number {
      color: #94a3b8;
    }

    .fc-event {
      border: none !important;
      font-size: 0.78rem;
      padding: 2px 5px;
      border-radius: 4px;
    }

    footer {
      max-width: 1100px;
      margin: 18px auto 0;
      text-align: center;
      color: #64748b;
      font-size: 0.85rem;
    }

    @media (max-width: 600px) {
      h1 { font-size: 1.25rem; }
      body { padding: 12px; }
    }
  </style>
</head>
<body>

  <header>
    <h1>Calendario Académico 2026</h1>
    <div class="subtitle">Ingeniería en Inteligencia Artificial e Inteligencia de Datos · UTS</div>
    
    <div class="legend">
      <div class="legend-item"><span class="dot encuentro"></span> Encuentro / Clase</div>
      <div class="legend-item"><span class="dot entrega"></span> Entrega de trabajo</div>
    </div>
  </header>

  <div id="calendar"></div>

  <footer>
    Solo Encuentros y Entregas · Semestre 2026-2 · Edita los eventos en el código si necesitas cambiar fechas
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/fullcalendar@6.1.15/index.global.min.js"></script>

  <script>
    document.addEventListener('DOMContentLoaded', function() {
      const calendarEl = document.getElementById('calendar');

      const calendar = new FullCalendar.Calendar(calendarEl, {
        initialView: 'dayGridMonth',
        initialDate: '2026-08-01',
        locale: 'es',
        height: 'auto',
        headerToolbar: {
          left: 'prev,next today',
          center: 'title',
          right: 'dayGridMonth,listMonth'
        },
        buttonText: {
          today: 'Hoy',
          month: 'Mes',
          list: 'Lista'
        },

        // ==========================================
        //  EVENTOS DEL SEMESTRE (solo Encuentros y Entregas)
        // ==========================================
        events: [

          // ---------- AGOSTO 2026 ----------
          { title: 'Encuentro – Introducción al curso', start: '2026-08-04T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-08-11T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-08-18T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-08-25T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Actividad 1 (Variables)', start: '2026-08-29', color: '#22c55e' },

          // ---------- SEPTIEMBRE 2026 ----------
          { title: 'Encuentro – Álgebra', start: '2026-09-01T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-09-08T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Actividad 2 (Técnica de modelado)', start: '2026-09-12', color: '#22c55e' },
          { title: 'Encuentro – Álgebra', start: '2026-09-15T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-09-22T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Actividad 3 (Modelo base / Notebook)', start: '2026-09-26', color: '#22c55e' },
          { title: 'Encuentro – Álgebra', start: '2026-09-29T18:30:00', color: '#3b82f6' },

          // ---------- OCTUBRE 2026 ----------
          { title: 'Encuentro – Álgebra', start: '2026-10-06T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Actividad 4 (Análisis exploratorio)', start: '2026-10-10', color: '#22c55e' },
          { title: 'Encuentro – Álgebra', start: '2026-10-13T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-10-20T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Bitácora de experimentación', start: '2026-10-24', color: '#22c55e' },
          { title: 'Encuentro – Álgebra', start: '2026-10-27T18:30:00', color: '#3b82f6' },

          // ---------- NOVIEMBRE 2026 ----------
          { title: 'Encuentro – Álgebra', start: '2026-11-03T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-11-10T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Dashboard + Informe ejecutivo', start: '2026-11-14', color: '#22c55e' },
          { title: 'Encuentro – Álgebra', start: '2026-11-17T18:30:00', color: '#3b82f6' },
          { title: 'Encuentro – Álgebra', start: '2026-11-24T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Avance Informe Final', start: '2026-11-28', color: '#22c55e' },

          // ---------- DICIEMBRE 2026 ----------
          { title: 'Encuentro – Álgebra', start: '2026-12-01T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Informe Final completo', start: '2026-12-05', color: '#22c55e' },
          { title: 'Encuentro – Cierre de curso', start: '2026-12-08T18:30:00', color: '#3b82f6' },
          { title: 'Entrega – Proyecto Final NutriFresh', start: '2026-12-12', color: '#22c55e' }
        ]
      });

      calendar.render();
    });
  </script>
</body>
</html>
