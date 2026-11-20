<script setup lang="ts">
useHead({ title: 'Profile — Sharina Adem' })

const personal = [
  { label: 'Name', value: 'Sharina Adem' },
  { label: 'Email', value: 'sharina.adem@carsu.edu.ph' },
  { label: 'Location', value: 'Butuan City, Philippines' },
]

const skills = [
  'Nuxt.js', 'Vue.js', 'JavaScript', 'TypeScript', 'HTML & CSS',
  'Tailwind CSS', 'UI/UX Design', 'Data Analysis', 'Mobile Development',
  'Project Management', 'Nest.js', 'C#', 'Android Studio + Kotlin',
]

const hobbies = ['Reading', 'Music', 'Fitness', 'Coding']
</script>

<template>
  <section class="mx-auto max-w-[1180px] px-5 py-10 md:px-8 md:py-16">
    <div class="mb-12 grid gap-8 border-b border-neutral-300 pb-10 md:grid-cols-[1fr_260px] md:items-end">
      <div>
        <p class="mb-4 font-mono text-xs font-bold uppercase tracking-[0.22em] text-black">Profile / 2026</p>
        <h1 class="text-5xl font-bold leading-none tracking-[-0.055em] text-black md:text-7xl">Personal<br />details.</h1>
      </div>
      <NuxtLink to="/" class="justify-self-start border-b border-black pb-1 font-mono text-xs font-bold uppercase tracking-[0.16em] text-neutral-700 transition-colors hover:text-black md:justify-self-end">
        ← Back home
      </NuxtLink>
    </div>

    <div class="grid gap-12 md:grid-cols-[0.72fr_1.28fr]">
      <div class="grid content-start gap-10">
        <ProfileAvatar />

        <div>
          <h2 class="mb-5 font-mono text-xs font-bold uppercase tracking-[0.2em] text-neutral-500">Personal information</h2>
          <dl class="border-t border-neutral-300">
            <div v-for="item in personal" :key="item.label" class="grid border-b border-neutral-300 py-4 md:grid-cols-[90px_1fr]">
              <dt class="font-mono text-xs uppercase tracking-wider text-neutral-500">{{ item.label }}</dt>
              <dd class="mt-1 text-sm font-semibold text-black md:mt-0">{{ item.value }}</dd>
            </div>
          </dl>
        </div>
      </div>

      <div class="border-l-0 border-neutral-300 md:border-l md:pl-12">
        <section class="border-b border-neutral-300 pb-10">
          <p class="mb-5 font-mono text-xs font-bold uppercase tracking-[0.2em] text-black">01 / Education</p>
          <h2 class="text-3xl font-bold tracking-tight text-black">Bachelor’s degree</h2>
          <p class="mt-3 text-lg text-neutral-600">Information Technology</p>
        </section>

        <section class="border-b border-neutral-300 py-10">
          <p class="mb-5 font-mono text-xs font-bold uppercase tracking-[0.2em] text-black">02 / Skills & interests</p>
          <div class="grid grid-cols-1 gap-x-8 gap-y-0 sm:grid-cols-2">
            <div v-for="(skill, index) in skills" :key="skill" class="flex items-center justify-between border-b border-neutral-300 py-3">
              <span class="font-semibold text-neutral-800">{{ skill }}</span>
              <span class="font-mono text-xs tabular-nums text-neutral-400">{{ String(index + 1).padStart(2, '0') }}</span>
            </div>
          </div>
        </section>

        <section class="py-10">
          <p class="mb-5 font-mono text-xs font-bold uppercase tracking-[0.2em] text-black">03 / Hobbies</p>
          <div class="flex flex-wrap gap-2">
            <span v-for="hobby in hobbies" :key="hobby" class="rounded-md border border-black px-4 py-2 text-sm font-semibold text-black">
              {{ hobby }}
            </span>
          </div>
        </section>
      </div>
    </div>
  </section>
</template>
