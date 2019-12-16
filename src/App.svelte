  <script>
    import { Link, Router, Route } from 'svelte-routing';
    import Login from '././Login.svelte';
    import RegisterUser from './components/users/RegisterUser.svelte';
    import ProfileUser from './components/users/ProfileUser.svelte';
    import Search from './components/users/Search.svelte';

    export let url = "";

  </script>

  <Router url="{url}">
    <nav>
	  <Link to='/'>Login</Link>
    <Link to='home'>Home</Link>
	  <Link to='buscar'>Buscar</Link>
    <Link to='perfil'>Perfil</Link>
	</nav>
	
	<div>
	  <Route path="/" component="{Login}" />
	  <Route path="perfil" component="{ProfileUser}" />
	  <Route path="buscar" component="{Search}" />
	  <Route path="registro" component="{RegisterUser}"></Route>
	</div>
  </Router>

<style>

</style>