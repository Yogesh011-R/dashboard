<script>
  import Home from './pages/Home.svelte';
  import { Router, Link, Route } from 'svelte-routing';

  import List from './pages/List.svelte';
  import Single from './pages/Single.svelte';
  import New from './pages/New.svelte';
</script>

<main>
  <Router>
    <Route path="/"><Home /></Route>
    <!-- Users -->
    <Route path="/users"><List /></Route>
    <Route path="/users/:userId"><Single /></Route>
    <Route path="/users/new"><New /></Route>

    <!-- Products -->
    <Route path="/products"><List /></Route>
    <Route path="/products/:productId"><Single /></Route>
    <Route path="/products/new"><New /></Route>
  </Router>
</main>
