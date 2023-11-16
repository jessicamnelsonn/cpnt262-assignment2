<script>
	import '../../app.postcss';
  import { AppShell, AppBar } from '@skeletonlabs/skeleton';
</script>

<AppShell>
	<AppBar>
		<svelte:fragment slot="lead"><a
		class="btn btn-sm variant-ghost-surface"
		href="https://discord.gg/EXqV7W8MtY"
		target="_blank"
		rel="noreferrer"
	>
		Discord
	</a>
	<a
		class="btn btn-sm variant-ghost-surface"
		href="https://twitter.com/SkeletonUI"
		target="_blank"
		rel="noreferrer"
	>
		Twitter
	</a>
	<a
		class="btn btn-sm variant-ghost-surface"
		href="https://github.com/skeletonlabs/skeleton"
		target="_blank"
		rel="noreferrer"
	>
		GitHub
	</a></svelte:fragment>
		<svelte:fragment slot="trail"><section class="text-4xl">Contact Us</section></svelte:fragment>
	</AppBar>
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
	<svelte:fragment slot="footer">
    &copy; Jessica Nelson 2023
  </svelte:fragment>
</AppShell>