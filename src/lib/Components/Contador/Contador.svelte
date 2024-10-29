<script>

   import "./contador.css"
   let contador = 0
  
  const sumar = () => {
    contador+=1;
  }

  const restar = () => {
    if( contador <= 0){
        contador = 0;
        return;
    }
    contador-=1;
  }

  const resetear = () => {
    contador = 0;
  }

</script>

<button on:click={sumar}>+</button>
<button on:click={restar}>-</button>
<button on:click={resetear}>Resetear</button>

<p>{contador}</p>
