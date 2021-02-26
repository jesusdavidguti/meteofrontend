<script>
    import { onMount, getContext } from "svelte";
    import { jsonData }            from "./store.js";
  
    import Buscar                  from "./Buscar.svelte";
    import Prevision                 from "./Prevision.svelte";
    import Boton                   from "./Boton.svelte";
  
    const URL = getContext("URL");
  
    let busqueda = "";
    let prevision = {};
  
    onMount(async () => {
      const response = await fetch(URL.previsiones);
      const data = await response.json();
      $jsonData = data;
    });
  
    $: regex = new RegExp(busqueda, "i");
    $: datos = busqueda 
      ? $jsonData.filter(item => regex.test(item.descripcion))
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
  
  <h1>PREVISIONES</h1>
  <Buscar bind:busqueda />
  
  <div class="container">
    <Prevision bind:prevision>
      <div style="text-align: right">
        <Boton documento={prevision} tipo="insertar" coleccion="clientes" />
      </div>
    </Prevision>
  </div>
  
  <div class="container">
    {#each datos as prevision}
      <Prevision {prevision}>
        <div style="text-align: right">
          <Boton documento={prevision} tipo="modificar" coleccion="previsiones" />
          <Boton documento={prevision} tipo="eliminar" coleccion="previsiones" />
        </div>
      </Prevision>
    {/each}
  </div>