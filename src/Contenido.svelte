<script>
  import { Route }  from "svelte-routing";
  import Inicio     from "./Inicio.svelte";
  import Articulos  from "./Articulos.svelte";
  import Clientes   from "./Clientes.svelte";
</script>

<style>
  /* Aquí el código CSS */
  /* Consultar el código fuente */
</style>

<main>
  <!-- Se eliminan etiquetas html para resaltar lo esencial -->
  <!-- Consulta el código fuente. --> 
  <Route path="/"           component={Inicio} />
  <Route path="/articulos"  component={Articulos} />
  <Route path="/clientes"   component={Clientes} />
</main>