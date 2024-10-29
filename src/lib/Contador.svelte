<script>
    let count = 0;
    const incrementar = () => {
        count += 1;
    };
    const restar = () => {
        if(count>0) count -= 1;
    };
</script>

<button on:click={incrementar}> Sumar </button>
<button on:click={restar}> Restar </button>
<p>La cuenta es {count}</p>
