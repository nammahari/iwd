<script lang="ts">
    import { agenda1 , agenda2 } from "$lib/data/data";
    import { createEventDispatcher } from 'svelte';
    import { clsx } from '$lib/utils';
    const dispatcher = createEventDispatcher();
</script>

<section id="Agenda" class="flex w-full flex-col items-center space-y-6 px-6 md:px-20 lg:px-24">
    <div class="pt-12 sm:pt-16 lg:pt-20">
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
          <div class="text-center">
            <h2
              class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl lg:text-5xl"
            >
              Our Agenda
            </h2>
            <p class="mt-4  text-gray-600 sm:text-xl">
              We have a fantastic lineup of speakers and sessions.
            </p>
          </div>
        </div>
      </div>

      <div class="flex flex-col items-center gap-20 px-5 py-20 md:flex-row md:items-start md:py-5">
        <div><ol role="list" class={clsx("space-y-8 bg-white/60 px-10 py-14 text-center shadow-xl shadow-blue-900/5")}>
            <h1 class="uppercase font-semibold tracking-wide text-orange-500">Day 1</h1>
            {#each agenda1 as item,i}
            <li
			aria-label={`${item.speaker} talking about ${item.title} at ${item.start} - ${item.end} IST`}
		>
        {#if i > 0}
				<div class="mx-auto mb-8 h-px w-48 bg-gray-500/10" />
			{/if}
            <h4
				class="text-lg font-semibold tracking-tight text-gray-900"
				tabindex={0}
			>
				{item.title}
			</h4>
            {#if item.speaker}
				<p class="mt-1 tracking-tight text-gray-900">
					{item.speaker}
				</p>
			{/if}
            <p class="mt-1 font-mono text-sm text-gray-500">
				<time dateTime={`T${item.start}-08:00`}>
					{item.start}
				</time>{' '}
				-{' '}
				<time dateTime={`T${item.end}-08:00`}>
					{item.end}
				</time>{' '}
				IST
			</p>
		</li>
            {/each}</div>
        <div><ol role="list" class={clsx("space-y-8 bg-white/60 px-10 py-14 text-center shadow-xl shadow-blue-900/5")}>
            <h1 class="uppercase font-semibold tracking-wide text-orange-500">Day 2</h1>
            {#each agenda2 as item,i}
            <li
			aria-label={`${item.speaker} talking about ${item.title} at ${item.start} - ${item.end} IST`}
		>
        {#if i > 0}
				<div class="mx-auto mb-8 h-px w-48 bg-gray-500/10" />
			{/if}
            <h4
				class="text-lg font-semibold tracking-tight text-gray-900"
				tabindex={0}
			>
				{item.title}
			</h4>
            {#if item.speaker}
				<p class="mt-1 tracking-tight text-gray-900">
					{item.speaker}
				</p>
			{/if}
            <p class="mt-1 font-mono text-sm text-gray-500">
				<time dateTime={`T${item.start}-08:00`}>
					{item.start}
				</time>{' '}
				-{' '}
				<time dateTime={`T${item.end}-08:00`}>
					{item.end}
				</time>{' '}
				IST
			</p>
		</li>
            {/each}</div>
        </div>
</section>