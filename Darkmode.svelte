<script>
    let fondo = true;
    let colorFondo = "grey";
    let colorFondo1 = "white";
    const cambiar = ()=>{
        if(fondo == true) fondo = false;
        else fondo = true;
    }
</script>

<button on:click={cambiar}>Cambiar fondo</button>
{#if fondo==true}
    <h2 style="background-color: {colorFondo}; color: {colorFondo1}">Hola</h2>
    {:else}
    <h2 style="background-color: {colorFondo1}; color: {colorFondo}">Hola</h2>
{/if}