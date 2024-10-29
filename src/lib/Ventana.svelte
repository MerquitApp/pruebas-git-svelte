<script>
    import logo from "/logo.png";
    export let imagenes = Array(3).fill(logo);
</script>
<style>
    .galeria {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 10px;
    }
  
    .galeria img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      object-fit: cover;
      cursor: pointer;
      transition: transform 0.2s;
    }
  
    .galeria img:hover {
      transform: scale(1.05);
    }
  </style>
  
  <div class="galeria">
    {#each imagenes as image}
      <img src={image} alt="imagen coche" />
    {/each}
  </div>