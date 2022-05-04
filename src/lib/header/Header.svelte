<script>
  import { page } from '$app/stores';
  import logo from './flow-logo.svg';
</script>

<nav class="container">
  <ul>
    <li>
      <img style="width:2em; height:2em;" src={logo} alt="Learn how to build on Flow" />
    </li>
  </ul>
  <ul>
    <li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
    <li class:active={$page.url.pathname === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
  </ul>
</nav>


