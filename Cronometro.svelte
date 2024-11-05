<script>
    let tiempo = 0;
    let intervalo;
    let enMarcha = false;
  
    // Función para iniciar el cronómetro
    function iniciar() {
      if (!enMarcha) {
        enMarcha = true;
        intervalo = setInterval(() => {
          tiempo += 1;
        }, 1000);
      }
    }
  
    // Función para pausar el cronómetro
    function pausar() {
      enMarcha = false;
      clearInterval(intervalo);
    }
  
    // Función para reiniciar el cronómetro
    function reiniciar() {
      tiempo = 0;
      enMarcha = false;
      clearInterval(intervalo);
    }
  
    // Formato de tiempo en minutos y segundos
    function formatearTiempo(t) {
      const minutos = Math.floor(t / 60);
      const segundos = t % 60;
      return `${String(minutos).padStart(2, '0')}:${String(segundos).padStart(2, '0')}`;
    }
  </script>
  
  <style>
    .cronometro {
      font-size: 2rem;
      margin: 1rem;
      text-align: center;
    }
    .botones {
      display: flex;
      justify-content: center;
      gap: 1rem;
    }
  </style>
  
  <div class="cronometro">
    <p>{formatearTiempo(tiempo)}</p>
    <div class="botones">
      <button on:click={iniciar} disabled={enMarcha}>Iniciar</button>
      <button on:click={pausar} disabled={!enMarcha}>Pausar</button>
      <button on:click={reiniciar}>Reiniciar</button>
    </div>
  </div>