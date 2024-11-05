<script>
    let tareas = [];
    let descripcion;
    let prioridad;

    function addTarea(){
        tareas.push({"descripcion":descripcion,"prioridad":prioridad})
    }

    function removeTask(index){
        tareas.splice(index,1)
    }

</script>



<div class="tarea">
    <div class="tarea-contenido">
        <h3>Modulo tareas prioridad</h3>
        <p>{descripcion}</p>
        <input type="text" placeholder="Descripción" bind:value={descripcion}>
        <select bind:value={prioridad}>
            <option value="1">Alta</option>
            <option value="2">Media</option>
            <option value="3">Baja</option>
        </select>

        <button on:click={addTarea}>Añadir tarea</button>

    </div>
</div>
{#each tareas as { descripcion, prioridad}, index}
<li class:alta={prioridad}>
    <div class="tarea">
        <div class="tarea-contenido">
            <h3>{descripcion}</h3>
            <p>{descripcion}</p>
            <button on:click={(removeTask(index))}>Eliminar tarea</button>
        </div>
    </div>
</li>

{/each}


<style>
    .tarea {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        border: 1px solid black;
        margin: 10px;
    }

    .tarea-contenido {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
    }
</style>