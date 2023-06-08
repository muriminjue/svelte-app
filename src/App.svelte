<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./pages/home.svelte";
  import About from "./pages/about.svelte";

  let url = "/";
</script>

<Router {url}>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
  </nav>
  <div>
    <Route path="/about" component={About} />
    <Route path="/"><Home /></Route>
  </div>
</Router>
