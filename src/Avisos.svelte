<script>
    import { onMount, getContext } from "svelte";
    import { jsonData }            from "./store.js";
  
    import Buscar                  from "./Buscar.svelte";
    import Aviso                   from "./Aviso.svelte";
    import Boton                   from "./Boton.svelte";
  
    const URL = getContext("URL");
  
    let busqueda = "";
    let aviso = {};
  
    onMount(async () => {
      const response = await fetch(URL.avisos);
      const data = await response.json();
      $jsonData = data;
    });
  
    $: regex = new RegExp(busqueda, "i");
    $: datos = busqueda 
      ? $jsonData.filter(item => regex.test(item.tipo))
      : $jsonData;
  
  </script>
  
  <style>
    .container {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: left;
      flex-wrap: wrap;
    }
  </style>
  
  <h1>AVISOS</h1>
  <Buscar bind:busqueda />
  
  <div class="container">
    <Aviso bind:aviso>
      <div style="text-align: right">
        <Boton documento={aviso} tipo="insertar" coleccion="avisos" />
      </div>
    </Aviso>
  </div>
  
  <div class="container">
    {#each datos as aviso}
      <Aviso {aviso}>
        <div style="text-align: right">
          <Boton documento={aviso} tipo="modificar" coleccion="avisos" />
          <Boton documento={aviso} tipo="eliminar" coleccion="avisos" />
        </div>
      </Aviso>
    {/each}
  </div>