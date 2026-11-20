<script setup lang="ts">
useHead({ title: 'Sharina Adem — Personal Profile' })
</script>

<template>
  <section class="mx-auto grid min-h-[calc(100vh-170px)] max-w-[1180px] lg:grid-cols-[1.08fr_0.92fr]">
    <div class="flex flex-col justify-between px-5 py-12 md:px-8 md:py-16 lg:border-r lg:border-neutral-300 lg:pr-14">
      <div>
        <p class="mb-8 font-mono text-xs font-bold uppercase tracking-[0.22em] text-black">Student / Developer / Designer</p>
        <h1 class="max-w-[720px] text-[clamp(3.8rem,9vw,7.5rem)] font-bold leading-[0.86] tracking-[-0.065em] text-black">
          Sharina
          <span class="block text-neutral-500">Adem.</span>
        </h1>
      </div>

      <div class="mt-16 grid gap-8 border-t border-neutral-300 pt-8 md:grid-cols-[1fr_auto] md:items-end">
        <div>
          <p class="mb-3 font-mono text-xs font-bold uppercase tracking-[0.18em] text-neutral-500">About me</p>
          <p class="max-w-[520px] text-xl leading-relaxed text-neutral-700">I am a student passionate about technology, design, and continuous learning.</p>
        </div>
        <NuxtLink to="/profile" class="inline-flex min-h-12 items-center justify-center rounded-md border border-black bg-black px-6 font-mono text-xs font-bold uppercase tracking-[0.16em] text-white transition-colors hover:bg-neutral-800">
          View profile ↗
        </NuxtLink>
      </div>
    </div>

    <aside class="flex items-center bg-neutral-50 px-5 py-10 md:px-10 lg:px-14">
      <div class="w-full"><ProfileAvatar /></div>
    </aside>
  </section>
</template>
