<script lang="ts">
  import Blur from '$lib/section/blur/Blur.svelte';
  import Hero from '$lib/section/hero/Hero.svelte';
  import Memories from '$lib/section/memories/Memories.svelte';
  import Sponsors from '$lib/section/sponsors/Sponsors.svelte';
  import Partners from '$lib/section/partners/Partners.svelte';
  import Tickets from '$lib/section/tickets/Tickets.svelte';
  import Why from '$lib/section/why/Why.svelte';
  import Cfp from '$lib/section/CFP/cfp.svelte'
  import Youtube from '$lib/section/youtube/youtube.svelte';
  import Corporate from '$lib/section/coporate Partners/corporate.svelte';
  import Agenda from '$lib/agenda/agenda.svelte';
</script>

<svelte:head>
  <title>WTM Chennai - IWD' 2024</title>
  <meta name="description" content="WTM Chennai - IWD' 2024" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#ffffff" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:site" content="@gdgchennai" />
  <meta name="twitter:creator" content="@gdgchennai" />
  <meta name="twitter:title" content="WTM Chennai - IWD' 2024" />
  <meta name="twitter:description" content="WTM Chennai - IWD' 2024" />
  <meta
    name="twitter:image"
    content="https://devfest.gdgchennai.in/gdgch-banner.png"
  />
  <meta property="og:type" content="website" />
  <meta property="og:title" content="WTM Chennai - IWD' 2024" />
  <meta property="og:description" content="WTM Chennai - IWD' 2024" />
  <meta property="og:site_name" content="WTM Chennai - IWD' 2024" />
  <meta property="og:url" content="https://devfest.gdgchennai.in/" />
  <meta
    property="og:image"
    content="https://devfest.gdgchennai.in/gdgch-banner.png"
  />
</svelte:head>

<div
  class="flex  flex-col items-center justify-start overflow-hidden p-8"
>
  <div class="space-y-16 md:space-y-44">
    <Blur />
    <Hero />
    <Why />
    <Agenda />
    <!-- <Tickets />
    <Sponsors />
    <Partners />
    <Corporate />
    <Memories /> -->
  </div>
</div>
