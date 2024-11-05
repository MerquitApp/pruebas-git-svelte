<script>
   import "./darkmode.css"
   let toogle = false;
   const toggleDarkMode = () => {
       toogle = !toogle;
   }
</script>

<button on:click={toggleDarkMode}>
   {toogle ? "Light Mode" : "Dark Mode"}
</button>

{#if toogle}
<div class="dark-mode-container">
    <p>Estamos en modo oscuro</p>
</div>
{:else}
<div class="light-mode-container">
    <p>Estamos en modo claro</p>
</div>
{/if}  