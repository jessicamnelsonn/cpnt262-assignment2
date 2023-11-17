<script>
  import '../../app.postcss';
  import { AppShell, AppBar, Avatar, Accordion, AccordionItem } from '@skeletonlabs/skeleton';

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
      <section class="text-3xl">Website Title.</section>
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
    <nav class="list-nav p-6 variant-filled text-secondary-100 hover:!text-primary-100">
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/blog">Blog</a></li>
        <li><a href="../contact">Contact</a></li>
      </ul>
    </nav>
  </svelte:fragment>

  <!-- Router Slot -->
  <slot />

  <Accordion class="card p-4 text-token">
    <AccordionItem open>
      <svelte:fragment slot="lead"></svelte:fragment>
      <svelte:fragment slot="summary">Section 1</svelte:fragment>
      <svelte:fragment slot="content">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Mollitia molestiae qui commodi hic atque laboriosam? Adipisci enim, deleniti aliquid incidunt odit, excepturi fugiat modi obcaecati consequatur et in perferendis molestiae.</svelte:fragment>
    </AccordionItem>
    <AccordionItem>
      <svelte:fragment slot="lead"> </svelte:fragment>
      <svelte:fragment slot="summary">Section 2</svelte:fragment>
      <svelte:fragment slot="content">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Mollitia molestiae qui commodi hic atque laboriosam? Adipisci enim, deleniti aliquid incidunt odit, excepturi fugiat modi obcaecati consequatur et in perferendis molestiae.</svelte:fragment>
    </AccordionItem>
    <AccordionItem>
      <svelte:fragment slot="lead"> </svelte:fragment>
      <svelte:fragment slot="summary">Section 3</svelte:fragment>
      <svelte:fragment slot="content">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Mollitia molestiae qui commodi hic atque laboriosam? Adipisci enim, deleniti aliquid incidunt odit, excepturi fugiat modi obcaecati consequatur et in perferendis molestiae.</svelte:fragment>
    </AccordionItem>
    <!-- ... -->
  </Accordion>

  <svelte:fragment slot="footer">
    <p class="p-2">&copy; Jessica Nelson 2023</p>
  </svelte:fragment>
</AppShell>
