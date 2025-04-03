<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
  <title>Control de Acabado</title>
  <style>
    :root {
      --bg-color: #f0f0f0;
      --text-color: #333;
      --primary-color: #007bff;
      --secondary-color: #6c757d;
      --success-color: #28a745;
      --danger-color: #dc3545;
      --warning-color: #ffc107;
      --header-bg: #343a40;
      --header-text: #fff;
      --button-text: #fff;
      --font-main: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html, body {
      height: 100%;
      font-family: var(--font-main);
      background-color: var(--bg-color);
      color: var(--text-color);
      overflow: hidden; /* Evita scroll general */
    }

    .app-container {
      display: flex;
      flex-direction: column;
      height: 100%;
    }

    header {
      background-color: var(--header-bg);
      color: var(--header-text);
      padding: 10px 15px;
      text-align: center;
      font-size: 1.2em;
    }
    header h1 {
      margin: 0;
      font-size: 1.3em;
    }

    main {
      flex-grow: 1;
      display: flex;
      flex-direction: column;
      overflow-y: auto;
      padding: 20px;
    }

    /* Vistas (ocultar/mostrar) */
    .view {
      display: none;
    }
    .view.active {
      display: block;
    }

    /* Botones básicos */
    .btn {
      padding: 10px 15px;
      font-size: 1em;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.2s ease;
      color: var(--button-text);
      text-align: center;
      margin: 5px 0;
      display: inline-block;
    }
    .btn-primary { background-color: var(--primary-color); }
    .btn-primary:hover { background-color: #0056b3; }
    .btn-secondary { background-color: var(--secondary-color); }
    .btn-secondary:hover { background-color: #5a6268; }
    .btn-success { background-color: var(--success-color); }
    .btn-success:hover { background-color: #218838; }
    .btn-danger { background-color: var(--danger-color); }
    .btn-danger:hover { background-color: #c82333; }
    .btn-warning { background-color: var(--warning-color); color: #333; }
    .btn-warning:hover { background-color: #e0a800; }
    .btn-large {
      padding: 15px 25px;
      font-size: 1.2em;
    }
    .btn-sm {
      font-size: 0.85em;
      padding: 5px 10px;
    }

    /* Menú principal (4 opciones) */
    .menu-buttons {
      display: flex;
      flex-direction: column;
      gap: 15px;
      max-width: 300px;
      margin: 40px auto;
      text-align: center;
    }
    .menu-buttons .btn {
      width: 100%;
    }

    /* --- Vista "Comenzar" (Operacional) --- */
    #empezar-view {
      display: flex;
      flex-direction: column;
      gap: 10px;
      height: 100%;
      position: relative;
    }
    #selected-part-label {
      font-size: 1em;
      font-weight: bold;
      text-align: center;
      margin-bottom: 5px;
    }

    .timer-section {
      flex-basis: 45%;
      background-color: var(--success-color);
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 15px;
      transition: background-color 0.3s ease;
      position: relative;
    }
    .timer-section.over-time {
      background-color: var(--danger-color);
    }
    .timer-display {
      font-size: 4em;
      font-weight: bold;
    }
    .target-time-display {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 0.9em;
      opacity: 0.9;
    }

    .counter-section {
      flex-basis: 55%;
      background-color: #fff;
      color: var(--text-color);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      position: relative;
    }
    .counter-display {
      font-size: 5em;
      font-weight: bold;
      color: var(--primary-color);
    }
    .target-pph-display {
      position: absolute;
      bottom: 10px;
      right: 15px;
      font-size: 0.9em;
      color: var(--secondary-color);
    }
    .current-hour-display {
      position: absolute;
      bottom: 10px;
      left: 15px;
      font-size: 0.9em;
      color: var(--secondary-color);
    }

    /* Botón corrección (dentro del contador) */
    #correction-button {
      position: absolute;
      left: 15px;
      top: 50%;
      transform: translateY(-50%);
      z-index: 20;
      width: 50px;
      height: 50px;
      font-size: 1.8em;
      line-height: 45px;
      text-align: center;
      border-radius: 50%;
      padding: 0;
    }

    /* Tap area */
    #tap-area {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 10; /* Botones estarán por arriba (z-index mayor). */
    }

    /* Start/Stop Controls */
    #start-stop-controls {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: center;
      padding: 5px 0;
      position: relative;
      z-index: 15;
    }
    #start-stop-controls .form-group {
      display: flex;
      flex-direction: column;
      margin: 5px 0;
    }
    #start-stop-controls label {
      font-size: 0.9em;
      margin-bottom: 3px;
    }
    #start-stop-controls input {
      width: 80px;
      padding: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1em;
    }

    /* Feedback Hora Completa */
    .hour-feedback {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 3em;
      color: white;
      z-index: 100;
      opacity: 0;
      transition: opacity 0.5s ease;
      pointer-events: none;
    }
    .hour-feedback.success {
      background-color: rgba(40, 167, 69, 0.9);
    }
    .hour-feedback.fail {
      background-color: rgba(220, 53, 69, 0.9);
    }
    .hour-feedback.visible {
      opacity: 1;
      pointer-events: auto;
    }

    /* --- Vista "Gestión de Piezas" --- */
    #piezas-view .form-group {
      margin-bottom: 15px;
    }
    #piezas-view label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }
    #piezas-view input,
    #piezas-view textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 1em;
    }
    #selected-part-label-gestor {
      font-size: 1em;
      font-weight: bold;
      margin: 10px 0;
    }

    .operations-list {
      margin-bottom: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      padding: 10px;
      background-color: #fff;
    }
    .operation-item {
      display: flex;
      gap: 10px;
      margin-bottom: 5px;
    }
    .operation-item input {
      flex: 1;
    }

    /* --- Vista "Histórico" --- */
    #historico-table-container table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }
    #historico-table-container th, 
    #historico-table-container td {
      border: 1px solid #ccc;
      padding: 8px;
      text-align: center;
      font-size: 0.9em;
    }
    #historico-table-container th {
      background-color: var(--secondary-color);
      color: #fff;
    }

    /* --- Vista "Configuración" --- */
    #settings-view .form-group {
      margin-bottom: 15px;
    }
    #settings-view label {
      font-weight: bold;
    }
    #settings-view fieldset {
      border: 1px solid #ccc;
      border-radius: 5px;
      padding: 10px;
      margin-bottom: 15px;
    }
    #settings-view legend {
      font-weight: bold;
      padding: 0 5px;
    }
    #settings-view .radio-group {
      margin: 5px 0;
    }
  </style>
</head>
<body>
  <div class="app-container">
    <header>
      <h1>Control de Acabado</h1>
    </header>

    <main>
      <!-- ========== MENÚ PRINCIPAL ========== -->
      <div id="menu-view" class="view active">
        <div class="menu-buttons">
          <button id="menu-comenzar-btn" class="btn btn-primary btn-large">Comenzar</button>
          <button id="menu-piezas-btn" class="btn btn-secondary btn-large">Gestión de Piezas</button>
          <button id="menu-historico-btn" class="btn btn-secondary btn-large">Histórico</button>
          <button id="menu-config-btn" class="btn btn-secondary btn-large">Configuración</button>
        </div>
      </div>

      <!-- ========== VISTA "COMENZAR" (Operacional) ========== -->
      <div id="empezar-view" class="view">
        <div id="selected-part-label">Pieza Seleccionada: <span id="selected-part-name">Ninguna</span></div>

        <div class="timer-section">
          <div class="target-time-display">Std: <span id="target-cycle-time-val">0</span>s</div>
          <div class="timer-display" id="chrono-display">0.0</div>
          <div>Tiempo de ciclo actual (s)</div>
        </div>

        <div class="counter-section">
          <button id="correction-button" class="btn btn-warning">-</button>
          <div class="current-hour-display">Hora: <span id="current-hour-val">--:--</span></div>
          <div class="target-pph-display">Meta: <span id="target-pph-val">0</span> PPH</div>
          <div class="counter-display" id="counter-val">0</div>
          <div>Piezas Esta Hora</div>
        </div>

        <div id="tap-area"></div>

        <div id="start-stop-controls">
          <div class="form-group">
            <label for="actual-operators">Operadores:</label>
            <input type="number" id="actual-operators" min="1" value="1">
          </div>
          <button id="start-btn" class="btn btn-success">START</button>
          <button id="stop-btn" class="btn btn-danger" style="display:none;">STOP</button>
          <!-- Nuevo botón "Guardar sin terminar" -->
          <button id="save-partial-btn" class="btn btn-warning" style="display:none;">Guardar sin terminar</button>
          <button id="back-menu-btn" class="btn btn-secondary">Menú Principal</button>
        </div>
      </div>

      <!-- ========== VISTA "GESTIÓN DE PIEZAS" ========== -->
      <div id="piezas-view" class="view">
        <h2>Gestión de Piezas</h2>

        <div id="selected-part-label-gestor">Pieza Seleccionada: <span id="current-part-gestor">Ninguna</span></div>

        <div class="form-group">
          <label for="part-number">Número de Parte:</label>
          <input type="text" id="part-number">
        </div>
        <div class="form-group">
          <label for="standard-pph">Piezas por Hora Estándar (PPH):</label>
          <input type="number" id="standard-pph" min="1">
        </div>
        <div class="form-group">
          <label for="standard-operators">Operadores Estándar:</label>
          <input type="number" id="standard-operators" min="1" value="1">
        </div>

        <div>
          <h3>Operaciones (opcional)</h3>
          <div class="operations-list" id="operations-list"></div>
          <button id="add-operation-btn" class="btn btn-warning">Agregar Operación</button>
        </div>

        <button id="save-part-btn" class="btn btn-primary btn-large">Guardar/Actualizar Pieza</button>
        <button id="load-part-list-btn" class="btn btn-secondary">Ver Piezas Guardadas</button>

        <div id="existing-parts" style="margin-top:20px;"></div>

        <button id="back-menu-piezas-btn" class="btn btn-secondary" style="margin-top:20px;">Menú Principal</button>
      </div>

      <!-- ========== VISTA "HISTÓRICO" ========== -->
      <div id="historico-view" class="view">
        <h2>Histórico</h2>
        <p>Registros de horas completas o guardados parciales. Incluye fecha, parte, operadores, piezas, etc.</p>
        <div id="historico-table-container" style="margin-top: 15px;"></div>
        <button id="back-menu-historico-btn" class="btn btn-secondary" style="margin-top:20px;">Menú Principal</button>
      </div>

      <!-- ========== VISTA "CONFIGURACIÓN" ========== -->
      <div id="settings-view" class="view">
        <h2>Configuración</h2>

        <fieldset>
          <legend>Inicio de Hora</legend>
          <div class="radio-group">
            <input type="radio" id="hour-start-zero" name="hour-start" value="0" checked>
            <label for="hour-start-zero">En punto (ej: 12:00 - 13:00)</label>
          </div>
          <div class="radio-group">
            <input type="radio" id="hour-start-thirty" name="hour-start" value="30">
            <label for="hour-start-thirty">A y media (ej: 12:30 - 13:30)</label>
          </div>
        </fieldset>

        <fieldset>
          <legend>Objetivo de Rendimiento</legend>
          <div class="radio-group">
            <input type="radio" id="target-standard" name="target-source" value="standard" checked>
            <label for="target-standard">Usar Estándar</label>
          </div>
          <div class="radio-group">
            <input type="radio" id="target-historical" name="target-source" value="historical">
            <label for="target-historical">Usar Mejor Histórico</label>
          </div>
          <p style="font-size: 0.9em; margin-top: 10px;">
            (Nota: Este ajuste sólo afecta el "tiempo estándar" y meta de PPH, 
            no el registro de datos en el histórico.)
          </p>
        </fieldset>

        <button id="save-settings-btn" class="btn btn-primary">Guardar Ajustes</button>
        <button id="back-menu-config-btn" class="btn btn-secondary" style="margin-top:15px;">Menú Principal</button>

        <hr style="margin:20px 0;">

        <button id="delete-all-data-btn" class="btn btn-danger" style="margin-top:10px;">Borrar TODOS los Datos</button>
      </div>

    </main>
  </div>

  <!-- Feedback de Hora Completa -->
  <div id="hour-feedback" class="hour-feedback">
    <span id="hour-feedback-text"></span>
  </div>

  <script>
  /*********************************************
   *          VARIABLES / ESTADOS GLOBALES
   *********************************************/
  let currentPartData = null; 
  let appSettings = {
    hourStartMinute: 0,       // 0 o 30
    targetSource: 'standard'  // 'standard' o 'historical'
  };

  let operationalState = {
    isRunning: false,
    currentHourCount: 0,
    chronoValue: 0.0,
    chronoInterval: null,
    mainInterval: null,
    targetCycleTime: 0,
    targetPph: 0,
    actualOperators: 1,
    lastTapTimestamp: 0,
    previousState: null,
    currentHourStartTime: null,
    nextHourEndTime: null
  };

  // Almacenamos TODOS los registros (hora completa o parciales) en un array
  // y luego lo guardamos en localStorage bajo la clave 'allRecords'
  // Estructura de cada registro:
  // {
  //   dateTime: string (fecha/hora guardado),
  //   partNumber: string,
  //   operators: number,
  //   count: number,
  //   minutes: number (duración real desde currentHourStartTime),
  //   pph: number (count / (minutes/60)),
  //   type: 'Completo' | 'Parcial'
  // }
  //
  // Nota: Para ver todos estos datos en el Histórico.
  //

  /*********************************************
   *       FUNCIONES DE LOCALSTORAGE
   *********************************************/
  function saveData(key, data) {
    try {
      localStorage.setItem(key, JSON.stringify(data));
    } catch (e) {
      console.error("Error guardando en localStorage:", e);
      alert("Error al guardar datos. El almacenamiento puede estar lleno o deshabilitado.");
    }
  }

  function loadData(key, defaultValue = null) {
    try {
      const data = localStorage.getItem(key);
      return data ? JSON.parse(data) : defaultValue;
    } catch (e) {
      console.error("Error cargando de localStorage:", e);
      return defaultValue;
    }
  }

  function loadAllParts() {
    return loadData('allPartsData', {});
  }
  function saveAllParts(parts) {
    saveData('allPartsData', parts);
  }

  function loadAllRecords() {
    return loadData('allRecords', []);
  }
  function saveAllRecords(records) {
    saveData('allRecords', records);
  }

  function loadAppSettings() {
    const loadedSettings = loadData('appSettings', appSettings);
    appSettings = { ...appSettings, ...loadedSettings };
  }
  function saveAppSettings() {
    saveData('appSettings', appSettings);
  }

  /*********************************************
   *             AUDIO
   *********************************************/
  let audioCtx = null;
  function initAudio() {
    if (!audioCtx) {
      try {
        audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      } catch (e) {
        console.warn("Web Audio API no soportada.");
      }
    }
  }

  function playTone(type = 'tap') {
    initAudio();
    if (!audioCtx) return;
    const osc = audioCtx.createOscillator();
    const gainNode = audioCtx.createGain();
    osc.connect(gainNode);
    gainNode.connect(audioCtx.destination);
    gainNode.gain.setValueAtTime(0.1, audioCtx.currentTime);

    if (type === 'success') {
      osc.type = 'sine';
      osc.frequency.setValueAtTime(660, audioCtx.currentTime);
      osc.frequency.linearRampToValueAtTime(880, audioCtx.currentTime + 0.1);
      gainNode.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 0.3);
      osc.start(audioCtx.currentTime);
      osc.stop(audioCtx.currentTime + 0.3);
    } else if (type === 'fail') {
      osc.type = 'square';
      osc.frequency.setValueAtTime(220, audioCtx.currentTime);
      osc.frequency.linearRampToValueAtTime(110, audioCtx.currentTime + 0.2);
      gainNode.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 0.4);
      osc.start(audioCtx.currentTime);
      osc.stop(audioCtx.currentTime + 0.4);
    } else {
      // tap
      osc.type = 'sine';
      osc.frequency.setValueAtTime(880, audioCtx.currentTime);
      gainNode.gain.exponentialRampToValueAtTime(0.0001, audioCtx.currentTime + 0.05);
      osc.start(audioCtx.currentTime);
      osc.stop(audioCtx.currentTime + 0.05);
    }
  }

  /*********************************************
   *        CAMBIO DE VISTAS
   *********************************************/
  function showView(viewId) {
    document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
    document.getElementById(viewId).classList.add('active');
  }

  /*********************************************
   *    ACTUALIZAR LABELS DE PIEZA SELECCIONADA
   *********************************************/
  const selectedPartNameEl = document.getElementById('selected-part-name');
  const currentPartGestorEl = document.getElementById('current-part-gestor');
  function updateSelectedPartLabels() {
    if (currentPartData) {
      selectedPartNameEl.textContent = currentPartData.partNumber;
      currentPartGestorEl.textContent = currentPartData.partNumber;
    } else {
      selectedPartNameEl.textContent = "Ninguna";
      currentPartGestorEl.textContent = "Ninguna";
    }
  }

  /*********************************************
   *         CÁLCULO DE OBJETIVOS
   *********************************************/
  const targetCycleTimeVal = document.getElementById('target-cycle-time-val');
  const targetPphVal = document.getElementById('target-pph-val');

  function calculateTargets() {
    if (!currentPartData) {
      targetPphVal.textContent = 0;
      targetCycleTimeVal.textContent = 0;
      return;
    }
    let stdPph = parseFloat(currentPartData.stdPph) || 1;
    let stdOps = parseInt(currentPartData.stdOps) || 1;
    let actualOps = operationalState.actualOperators;

    // Ratio = (PPH estándar / Ops estándar)
    let stdRatio = stdPph / stdOps;
    if (stdRatio <= 0) stdRatio = 1;

    // Si usas "historical" => En este demo no sacamos un "best ratio",
    // pero podrías derivarlo de tu propia lógica. 
    // Para ahora, usaremos siempre stdRatio:
    // (Podrías expandir si deseas soporte de "historical" vs "standard".)
    let chosenRatio = stdRatio;
    if (appSettings.targetSource === 'historical') {
      // Lógica para usar histórico si existiera. Por ahora, lo dejamos igual al stdRatio.
      // chosenRatio = ??? (no implementado en este ejemplo)
    }

    let targetPPH = chosenRatio * actualOps;
    if (targetPPH < 1) targetPPH = 1;
    let targetCycle = 3600 / targetPPH;

    operationalState.targetPph = Math.round(targetPPH);
    operationalState.targetCycleTime = parseFloat(targetCycle.toFixed(1));

    targetPphVal.textContent = operationalState.targetPph;
    targetCycleTimeVal.textContent = operationalState.targetCycleTime;
  }

  /*********************************************
   *   MOSTRADORES DE UI DEL CRONÓMETRO/CONTADOR
   *********************************************/
  const chronoDisplay = document.getElementById('chrono-display');
  const counterVal = document.getElementById('counter-val');
  const currentHourVal = document.getElementById('current-hour-val');
  const timerSection = document.querySelector('.timer-section');

  function updateChronoDisplay() {
    chronoDisplay.textContent = operationalState.chronoValue.toFixed(1);
    if (operationalState.chronoValue > operationalState.targetCycleTime) {
      timerSection.classList.add('over-time');
    } else {
      timerSection.classList.remove('over-time');
    }
  }

  function updateCounterDisplay() {
    counterVal.textContent = operationalState.currentHourCount;
  }

  function updateCurrentHourDisplay() {
    if (operationalState.currentHourStartTime && operationalState.nextHourEndTime) {
      const start = operationalState.currentHourStartTime;
      const end = operationalState.nextHourEndTime;
      const formatTime = (date) => date.toLocaleTimeString('es-ES', { hour: '2-digit', minute: '2-digit' });
      currentHourVal.textContent = `${formatTime(start)} - ${formatTime(end)}`;
    } else {
      currentHourVal.textContent = '--:--';
    }
  }

  /*********************************************
   *       LÓGICA DE TAP Y CORRECCIÓN
   *********************************************/
  const tapArea = document.getElementById('tap-area');
  const correctionButton = document.getElementById('correction-button');

  function handleTap(e) {
    // Evitar contar si el click es en un botón (z-index mayor) o en un child
    if (!operationalState.isRunning) return;
    // Asegurarnos de que se cliqueó en el "tap-area" en sí:
    if (e.target.id !== 'tap-area') return;

    playTone('tap');

    operationalState.previousState = {
      count: operationalState.currentHourCount,
      chronoValue: operationalState.chronoValue,
      tapTimestamp: Date.now()
    };

    operationalState.currentHourCount++;
    updateCounterDisplay();

    // Reiniciar crono
    operationalState.chronoValue = 0.0;
    operationalState.lastTapTimestamp = Date.now();
    updateChronoDisplay();
    timerSection.classList.remove('over-time');
  }

  function handleCorrection() {
    if (!operationalState.isRunning || !operationalState.previousState || operationalState.currentHourCount <= 0) {
      return;
    }
    // Restaura estado previo
    operationalState.currentHourCount = operationalState.previousState.count;
    let timeSinceLastTap = (Date.now() - operationalState.previousState.tapTimestamp)/1000;
    operationalState.chronoValue = operationalState.previousState.chronoValue + timeSinceLastTap;

    operationalState.previousState = null;
    updateCounterDisplay();
    updateChronoDisplay();
  }

  /*********************************************
   *           START / STOP / PARTIAL
   *********************************************/
  const startBtn = document.getElementById('start-btn');
  const stopBtn = document.getElementById('stop-btn');
  const savePartialBtn = document.getElementById('save-partial-btn');
  const backMenuBtn = document.getElementById('back-menu-btn');
  const actualOperatorsInput = document.getElementById('actual-operators');

  function startOperation() {
    operationalState.actualOperators = parseInt(actualOperatorsInput.value) || 1;
    if (!currentPartData) {
      alert("Selecciona o configura primero una pieza.");
      return;
    }

    operationalState.isRunning = true;
    operationalState.currentHourCount = 0;
    operationalState.chronoValue = 0.0;
    operationalState.previousState = null;
    updateCounterDisplay();
    updateChronoDisplay();

    calculateTargets();

    // Determinar inicio y fin de hora
    const now = new Date();
    let currentMinute = now.getMinutes();
    let startMinute = appSettings.hourStartMinute || 0;

    operationalState.currentHourStartTime = new Date(now);
    if (currentMinute < startMinute) {
      // Antes de la "marca" => Se cuenta la hora anterior
      operationalState.currentHourStartTime.setHours(now.getHours() - 1);
      operationalState.currentHourStartTime.setMinutes(startMinute, 0, 0);
    } else {
      operationalState.currentHourStartTime.setMinutes(startMinute, 0, 0);
    }
    operationalState.nextHourEndTime = new Date(operationalState.currentHourStartTime);
    operationalState.nextHourEndTime.setHours(operationalState.nextHourEndTime.getHours() + 1);
    updateCurrentHourDisplay();

    // Iniciar intervalos
    operationalState.chronoInterval = setInterval(() => {
      operationalState.chronoValue += 0.1;
      updateChronoDisplay();
    }, 100);
    operationalState.mainInterval = setInterval(checkHourEnd, 1000);

    // Ajustes de botones
    startBtn.style.display = 'none';
    stopBtn.style.display = 'inline-block';
    savePartialBtn.style.display = 'inline-block';
    backMenuBtn.disabled = true; 
    actualOperatorsInput.disabled = true;

    tapArea.style.pointerEvents = 'auto';
    correctionButton.style.display = 'block';
  }

  function stopOperation() {
    operationalState.isRunning = false;
    clearInterval(operationalState.chronoInterval);
    clearInterval(operationalState.mainInterval);
    operationalState.chronoInterval = null;
    operationalState.mainInterval = null;

    startBtn.style.display = 'inline-block';
    stopBtn.style.display = 'none';
    savePartialBtn.style.display = 'none';
    backMenuBtn.disabled = false;
    actualOperatorsInput.disabled = false;

    tapArea.style.pointerEvents = 'none';
    correctionButton.style.display = 'none';
    currentHourVal.textContent = '--:--';
  }

  function checkHourEnd() {
    if (!operationalState.isRunning) return;
    const now = new Date();
    if (now >= operationalState.nextHourEndTime) {
      // Se cumplió la hora
      const achievedCount = operationalState.currentHourCount;
      // Para mostrar feedback (opcional)
      let success = (achievedCount >= operationalState.targetPph);

      // Guardar en histórico
      saveCurrentSession(false);  // false => no es parcial (es "Completo")

      // Feedback (opcional)
      showHourFeedback(success, achievedCount, operationalState.targetPph);
      playTone(success ? 'success' : 'fail');

      // Preparar la siguiente hora
      operationalState.currentHourCount = 0;
      operationalState.chronoValue = 0.0;
      operationalState.previousState = null;
      updateCounterDisplay();
      updateChronoDisplay();
      timerSection.classList.remove('over-time');

      operationalState.currentHourStartTime = new Date(operationalState.nextHourEndTime);
      operationalState.nextHourEndTime = new Date(operationalState.currentHourStartTime);
      operationalState.nextHourEndTime.setHours(operationalState.nextHourEndTime.getHours() + 1);
      updateCurrentHourDisplay();
    }
  }

  // Guarda el registro actual (ya sea parcial o completo) en el Histórico
  function saveCurrentSession(isPartial) {
    if (!currentPartData) return;

    const now = new Date();
    // Tiempo transcurrido en ms
    let durationMs = now - operationalState.currentHourStartTime;
    if (durationMs < 0) durationMs = 0;
    const minutes = durationMs / (1000 * 60);

    let count = operationalState.currentHourCount;
    // pph = count / (tiempoEnHoras)
    let pph = 0;
    if (minutes > 0) {
      pph = count / (minutes / 60);
    }

    const record = {
      dateTime: now.toLocaleString('es-ES'), // Ej: "2/04/2025 12:34:56"
      partNumber: currentPartData.partNumber,
      operators: operationalState.actualOperators,
      count: count,
      minutes: parseFloat(minutes.toFixed(1)),
      pph: parseFloat(pph.toFixed(1)),
      type: isPartial ? "Parcial" : "Completo"
    };

    let allRecs = loadAllRecords();
    allRecs.push(record);
    saveAllRecords(allRecs);
  }

  /*********************************************
   *         FEEDBACK VISUAL DE HORA
   *********************************************/
  const hourFeedback = document.getElementById('hour-feedback');
  const hourFeedbackText = document.getElementById('hour-feedback-text');

  function showHourFeedback(success, achieved, target) {
    hourFeedback.classList.remove('success','fail');
    if (success) {
      hourFeedback.classList.add('success');
      hourFeedbackText.textContent = `¡Meta Cumplida! (${achieved}/${target})`;
    } else {
      hourFeedback.classList.add('fail');
      hourFeedbackText.textContent = `Meta No Cumplida (${achieved}/${target})`;
    }
    hourFeedback.classList.add('visible');
    setTimeout(() => {
      hourFeedback.classList.remove('visible');
    }, 2500);
  }

  /*********************************************
   *           ADMIN. DE PIEZAS
   *********************************************/
  const partNumberInput = document.getElementById('part-number');
  const standardPphInput = document.getElementById('standard-pph');
  const standardOperatorsInput = document.getElementById('standard-operators');
  const savePartBtn = document.getElementById('save-part-btn');
  const loadPartListBtn = document.getElementById('load-part-list-btn');
  const existingPartsDiv = document.getElementById('existing-parts');
  const addOperationBtn = document.getElementById('add-operation-btn');
  const operationsList = document.getElementById('operations-list');

  function listAllPartsInDiv() {
    const allParts = loadAllParts();
    const keys = Object.keys(allParts);
    existingPartsDiv.innerHTML = '';

    if (keys.length === 0) {
      existingPartsDiv.innerHTML = '<p>No hay piezas guardadas.</p>';
      return;
    }
    const ul = document.createElement('ul');
    ul.style.listStyle = 'none';
    ul.style.paddingLeft = '0';

    keys.forEach(k => {
      const li = document.createElement('li');
      li.style.marginBottom = '10px';
      const p = allParts[k];
      li.innerHTML = `
        <strong>${p.partNumber}</strong> 
        (PPH: ${p.stdPph}, Ops: ${p.stdOps})
        <button data-part="${k}" class="btn btn-primary btn-sm" style="margin-left:10px;">Cargar</button>
      `;
      ul.appendChild(li);
    });
    existingPartsDiv.appendChild(ul);

    ul.querySelectorAll('button').forEach(btn => {
      btn.addEventListener('click', () => {
        const partKey = btn.getAttribute('data-part');
        const allP = loadAllParts();
        if (allP[partKey]) {
          currentPartData = allP[partKey];
          updateSelectedPartLabels();
          alert(`Pieza "${partKey}" cargada.`);
        }
      });
    });
  }

  function saveOrUpdateCurrentPart() {
    const pn = partNumberInput.value.trim();
    const stdPPH = parseInt(standardPphInput.value) || 1;
    const stdOps = parseInt(standardOperatorsInput.value) || 1;

    if (!pn) {
      alert("Debes ingresar un Número de Parte.");
      return;
    }
    const opItems = [...operationsList.querySelectorAll('.operation-item')].map(item => {
      const name = item.querySelector('.op-name').value.trim();
      const time = parseFloat(item.querySelector('.op-time').value) || 0;
      return { name, time };
    });

    let allParts = loadAllParts();
    let existing = allParts[pn] || {};

    // Conservar data previa si quieres, en este caso simplemente sobrescribimos
    const updatedPartData = {
      partNumber: pn,
      stdPph: stdPPH,
      stdOps: stdOps,
      operations: opItems
    };
    allParts[pn] = updatedPartData;
    saveAllParts(allParts);

    currentPartData = updatedPartData;
    updateSelectedPartLabels();
    alert("Pieza guardada/actualizada correctamente.");
  }

  function addOperationField() {
    const div = document.createElement('div');
    div.className = 'operation-item';
    div.innerHTML = `
      <input type="text" placeholder="Nombre Operación" class="op-name">
      <input type="number" placeholder="Tiempo (s)" class="op-time" style="width:100px;">
      <button class="btn btn-danger btn-sm">X</button>
    `;
    operationsList.appendChild(div);

    div.querySelector('button').addEventListener('click', () => {
      operationsList.removeChild(div);
    });
  }

  /*********************************************
   *         HISTÓRICO: MOSTRAR TODO
   *********************************************/
  const historicoTableContainer = document.getElementById('historico-table-container');

  function showHistorico() {
    const records = loadAllRecords();
    if (!records || records.length === 0) {
      historicoTableContainer.innerHTML = '<p>No hay registros en el histórico.</p>';
      return;
    }
    let html = `
      <table>
        <thead>
          <tr>
            <th>Fecha/Hora</th>
            <th>Parte</th>
            <th>Operadores</th>
            <th>Piezas</th>
            <th>Minutos</th>
            <th>PPH</th>
            <th>Tipo</th>
          </tr>
        </thead>
        <tbody>
    `;
    records.forEach(rec => {
      html += `
        <tr>
          <td>${rec.dateTime}</td>
          <td>${rec.partNumber}</td>
          <td>${rec.operators}</td>
          <td>${rec.count}</td>
          <td>${rec.minutes}</td>
          <td>${rec.pph}</td>
          <td>${rec.type}</td>
        </tr>
      `;
    });
    html += `</tbody></table>`;
    historicoTableContainer.innerHTML = html;
  }

  /*********************************************
   *         CONFIGURACIÓN
   *********************************************/
  const hourStartZeroRadio = document.getElementById('hour-start-zero');
  const hourStartThirtyRadio = document.getElementById('hour-start-thirty');
  const targetStandardRadio = document.getElementById('target-standard');
  const targetHistoricalRadio = document.getElementById('target-historical');
  const saveSettingsBtn = document.getElementById('save-settings-btn');

  /*********************************************
   *       BORRAR TODOS LOS DATOS
   *********************************************/
  const deleteAllDataBtn = document.getElementById('delete-all-data-btn');

  /*********************************************
   *          EVENT LISTENERS
   *********************************************/
  // Menú principal
  document.getElementById('menu-comenzar-btn').addEventListener('click', () => {
    showView('empezar-view');
    updateSelectedPartLabels();
  });
  document.getElementById('menu-piezas-btn').addEventListener('click', () => {
    showView('piezas-view');
    updateSelectedPartLabels();
  });
  document.getElementById('menu-historico-btn').addEventListener('click', () => {
    showHistorico();
    showView('historico-view');
  });
  document.getElementById('menu-config-btn').addEventListener('click', () => {
    // Cargar los ajustes en la UI
    hourStartZeroRadio.checked = (appSettings.hourStartMinute === 0);
    hourStartThirtyRadio.checked = (appSettings.hourStartMinute === 30);
    targetStandardRadio.checked = (appSettings.targetSource === 'standard');
    targetHistoricalRadio.checked = (appSettings.targetSource === 'historical');
    showView('settings-view');
  });

  // Vista Comenzar
  tapArea.addEventListener('click', handleTap);
  correctionButton.addEventListener('click', handleCorrection);
  startBtn.addEventListener('click', startOperation);
  stopBtn.addEventListener('click', stopOperation);

  // Botón "Guardar sin terminar"
  savePartialBtn.addEventListener('click', () => {
    if (!operationalState.isRunning) {
      return;
    }
    // Guardamos la data como parcial y detenemos la operación
    saveCurrentSession(true); // true => Parcial
    stopOperation();
    alert("Se guardó el registro de forma parcial y se detuvo la operación.");
  });

  backMenuBtn.addEventListener('click', () => {
    if (operationalState.isRunning) {
      alert("Primero presiona STOP o 'Guardar sin terminar'.");
      return;
    }
    showView('menu-view');
  });

  actualOperatorsInput.addEventListener('change', () => {
    operationalState.actualOperators = parseInt(actualOperatorsInput.value) || 1;
    if (!operationalState.isRunning) {
      calculateTargets();
    }
  });

  // Vista Piezas
  savePartBtn.addEventListener('click', saveOrUpdateCurrentPart);
  loadPartListBtn.addEventListener('click', listAllPartsInDiv);
  document.getElementById('back-menu-piezas-btn').addEventListener('click', () => {
    showView('menu-view');
  });
  addOperationBtn.addEventListener('click', addOperationField);

  // Vista Histórico
  document.getElementById('back-menu-historico-btn').addEventListener('click', () => {
    showView('menu-view');
  });

  // Vista Configuración
  saveSettingsBtn.addEventListener('click', () => {
    appSettings.hourStartMinute = hourStartThirtyRadio.checked ? 30 : 0;
    appSettings.targetSource = targetHistoricalRadio.checked ? 'historical' : 'standard';
    saveAppSettings();
    calculateTargets();
    alert("Ajustes guardados.");
    showView('menu-view');
  });
  document.getElementById('back-menu-config-btn').addEventListener('click', () => {
    showView('menu-view');
  });

  // Borrar TODOS los datos
  deleteAllDataBtn.addEventListener('click', () => {
    if (!confirm("¿Borrar TODOS los datos? Esta acción es irreversible.")) return;
    localStorage.removeItem('allPartsData');
    localStorage.removeItem('allRecords');
    localStorage.removeItem('appSettings');
    alert("Datos borrados. Se recargará la app.");
    location.reload();
  });

  /*********************************************
   *         AL CARGAR LA PÁGINA
   *********************************************/
  window.addEventListener('load', () => {
    loadAppSettings();
    tapArea.style.pointerEvents = 'none';  // Desactivar tap hasta START
    correctionButton.style.display = 'none';
    updateSelectedPartLabels();
  });
  window.addEventListener('beforeunload', () => {
    // Si deseas guardar la última pieza usada:
    // localStorage.setItem('lastUsedPartNumber', currentPartData ? currentPartData.partNumber : '');
  });
  </script>
</body>
</html>
