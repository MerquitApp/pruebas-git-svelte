<script>
  import Header from "./lib/Header.svelte";
  import Contador from "./lib/Contador.svelte";
  import Darkmode from "./lib/Darkmode.svelte";
  import Ventana from "./lib/Ventana.svelte";
  import Cronometro from "./lib/Cronometro.svelte";

  let colores = ['blue', 'red', 'green', 'yellow', 'black']
</script>

<main>
  {#each colores as color, i}
    {#if i%2}
      <Header {color} titulo={color} tam={3}/>
      {:else}
      <Header {color} titulo={color} tam={2}/>
    {/if}
  {/each}
  <Contador></Contador>
  <Darkmode></Darkmode>
  <Ventana></Ventana>
  <Cronometro></Cronometro>
</main>