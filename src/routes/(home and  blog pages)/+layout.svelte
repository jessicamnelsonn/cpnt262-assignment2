<script>
  import '../../app.postcss';
  import { AppShell, AppBar, Avatar } from '@skeletonlabs/skeleton';

  let navigation = [
    { name: "Home", href: "/" },
    { name: "Blog", href: "/blog" },
    { name: "Contact", href: "/contact" }
  ];
</script>

<AppShell>
  <svelte:fragment slot="header">
    <AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
      <svelte:fragment slot="lead">
        <Avatar
          src="images/hero-skeleton-ui.jpg"
          width="w-20"
          rounded="rounded-md"
          border="border-4 border-surface-300-600-token hover:!border-red-200"
          cursor="cursor-pointer" />
      </svelte:fragment>
      <section class="text-3xl"> Website Title.</section>
      <svelte:fragment slot="trail">
        <nav>
          <ul class="flex">
            {#each navigation as { name, href }}
              <li><a class="p-2" {href}>{name}</a></li>
            {/each}
          </ul>
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

  <svelte:fragment slot="footer">
    <p class="p-2">&copy; Jessica Nelson 2023</p>
  </svelte:fragment>
</AppShell>