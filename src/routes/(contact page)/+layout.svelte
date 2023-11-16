<script>
	import '../../app.postcss';
  import { AppShell, AppBar } from '@skeletonlabs/skeleton';
</script>

<AppShell>
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