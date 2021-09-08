<script>
  // https://blog.logrocket.com/how-to-build-responsive-navbar-tailwind-css/
	import { url } from '@roxi/routify'
  import Fa from 'svelte-fa';
	// import { Goto}
  import { faBars } from '@fortawesome/free-solid-svg-icons'
  let menu = false;
</script>

<nav class="flex flex-wrap items-center justify-between w-full py-4 md:py-0 px-4 text-lg text-gray-700 bg-white">
	<div>
		<a href=".">
			TU LOGO
		</a>
		<span id="menu-button" class="h-6 w-6 cursor-pointer md:hidden block" on:click={() => {menu = !menu}}>
			<Fa icon={faBars} />
		</span>
	</div>

	<div class:hidden={!menu} class="hidden w-full md:flex md:items-center md:w-auto " id="menu">
		<ul class="text-base text-gray-700 pt-4 md:flex md:justify-between md:pt-0">
			<li>
				<a class="md:p-4 py-2 block hover:text-purple-400" href=".">La Empresa</a>
			</li>
			<li>
				<a class="md:p-4 py-2 block hover:text-purple-400" href=".">Servicios</a>
			</li>
			<li>
				<a class="md:p-4 py-2 block hover:text-purple-400" href=".">Blog</a>
			</li>
			<li>
				<a class="md:p-4 py-2 block hover:text-purple-400" href=".">Contacto</a>
			</li>
			<li>
				<a class="md:p-4 py-2 block hover:text-purple-400 text-purple-500" href=".">Login</a>
			</li>
		</ul>
	</div>

</nav>
