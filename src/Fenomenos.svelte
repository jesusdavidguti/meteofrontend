<script>
    import { onMount, getContext } from "svelte";
    import { jsonData }            from "./store.js";
  
    import Buscar                  from "./Buscar.svelte";
    import Fenomeno                 from "./Fenomeno.svelte";
    import Boton                   from "./Boton.svelte";
  
    const URL = getContext("URL");
  
    let busqueda = "";
    let fenomeno = {};
  
    onMount(async () => {
      const response = await fetch(URL.fenomenos);
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
  
  <h1>FENOMENOS</h1>
  <Buscar bind:busqueda />
  
  <div class="container">
    <Fenomeno bind:fenomeno>
      <div style="text-align: right">
        <Boton documento={fenomeno} tipo="insertar" coleccion="fenomenos" />
      </div>
    </Fenomeno>
  </div>
  
  <div class="container">
    {#each datos as fenomeno}
      <Fenomeno {fenomeno}>
        <div style="text-align: right">
          <Boton documento={fenomeno} tipo="modificar" coleccion="fenomenos" />
          <Boton documento={fenomeno} tipo="eliminar" coleccion="fenomenos" />
        </div>
      </Fenomeno>
    {/each}
  </div>