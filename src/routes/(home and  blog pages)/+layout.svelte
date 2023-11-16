<script>
	import '../../app.postcss';
  import { AppShell, AppBar, Avatar } from '@skeletonlabs/skeleton';
</script>

<AppShell>
	<svelte:fragment slot="header">
    <AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
        <Avatar 
        src="https://picsum.photos/id/159/200/300" 
        width="w-20" 
        rounded="rounded-md" 
        border="border-4 border-surface-300-600-token hover:!border-red-200"
        cursor="cursor-pointer"/>
      </svelte:fragment>
	<section class="text-3xl">My Website Title.</section>
  <svelte:fragment slot="trail"> 
  <nav class="flex list-nav list-none">
		<li><a href="/">Home</a></li>
		<li><a href="/blog">Blog</a></li>
		<li><a href="/contact">Contact</a></li>
  </nav>  
</svelte:fragment>
			
		</AppBar>
  </svelte:fragment>

	<svelte:fragment slot="sidebarLeft">
		<nav class="list-nav p-2">
			<ul>
				<li><a href="/">Home</a></li>
				<li><a href="/blog">Blog</a></li>
				<li><a href="../contact">Contact</a></li>
			</ul>
		</nav>
  </svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->

	<!-- (pageFooter) -->
	<svelte:fragment slot="footer">
    &copy; Jessica Nelson 2023
  </svelte:fragment>
</AppShell>