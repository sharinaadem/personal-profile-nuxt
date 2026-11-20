<template>
  <div class="min-h-screen">
    <header class="border-b border-neutral-300/80 bg-white/95 backdrop-blur">
      <nav class="mx-auto flex max-w-[1180px] items-center justify-between px-5 py-5 md:px-8">
        <NuxtLink to="/" class="font-mono text-sm font-bold uppercase tracking-[0.18em] text-black" aria-label="Sharina Adem, homepage">
          SA<span>.</span>
        </NuxtLink>

        <div class="flex items-center gap-1 border-l border-neutral-300 pl-3 md:gap-4 md:pl-6">
          <NuxtLink to="/" class="rounded-md px-3 py-2 font-mono text-xs font-bold uppercase tracking-widest text-neutral-600 transition-colors hover:text-black" active-class="text-black">
            Home
          </NuxtLink>
          <NuxtLink to="/profile" class="rounded-md border border-black bg-black px-4 py-2 font-mono text-xs font-bold uppercase tracking-widest text-white transition-colors hover:bg-neutral-800" active-class="bg-neutral-800">
            Profile
          </NuxtLink>
        </div>
      </nav>
    </header>

    <main><slot /></main>

    <footer class="border-t border-neutral-300">
      <div class="mx-auto flex max-w-[1180px] flex-col gap-2 px-5 py-6 font-mono text-xs uppercase tracking-[0.14em] text-neutral-500 md:flex-row md:items-center md:justify-between md:px-8">
        <span>Sharina Adem / Personal Profile</span>
        <span>Butuan City · Philippines</span>
      </div>
    </footer>
  </div>
</template>
