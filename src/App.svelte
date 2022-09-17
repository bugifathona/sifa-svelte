<script>
  import Router from 'svelte-spa-router';
  import FixedHeader from './components/navigations/FixedHeader.svelte';
  import Academic from './pages/Academic.svelte';
  import Finance from './pages/Finance.svelte';
  import Home from './pages/Home.svelte';
  import NotFound from './pages/NotFound.svelte';
  import Reference from './pages/Reference.svelte';
  
  const routes = {
    "/": Home,
    "/reference": Reference,
    "/reference/*": Reference,
    "/academic": Academic,
    "/academic/*": Academic,
    "/finance": Finance,
    "/finance/*": Finance,
    "*": NotFound
  }

  const navLinks = [
    {
      title: "Home",
      link: "/"
    },
    {
      title: "Reference",
      link: "/reference"
    },
    {
      title: "Academic",
      link: "/academic"
    },
    {
      title: "Finance",
      link: "/finance"
    },
  ]

</script>

<FixedHeader {navLinks} />

<Router {routes} />