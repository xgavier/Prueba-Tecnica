<script>
  import Navbar from "../Components/Navbar/navbar.svelte";
  import Inicio from "../Components/Pages/+inicio.svelte";
  import Articulo from "../Components/Pages/articulos.svelte";
  import Contacto from "../Components/Pages/contacto.svelte";
  import { Router, Link, Route } from "svelte-routing";
</script>

<div>
    <Router>
  <Navbar />
  <Route path="/">
    <Inicio />
  </Route>
  <Route path="/Articulo">
<Articulo></Articulo>
</Route>
<Route path="/Contacto">
    <Contacto></Contacto>
    </Route>
</Router>
</div>

<style>
  :global(body) {
    background-image: url("https://www.schgroup.com/wp-content/uploads/2019/05/Primary-600x315-cropped.png");
  }
</style>
