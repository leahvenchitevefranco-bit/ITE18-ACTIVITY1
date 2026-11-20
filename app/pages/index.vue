<script setup lang="ts">
useSeoMeta({
  title: 'Kuring | Personal Portfolio',
  description:
    'Hi, I am Leahvenchiteve M. Franco (Kuring), an Information Technology student at Caraga State University.',
})

const facts = [
  { label: 'Course', value: 'Bachelor of Science in Information Technology' },
  { label: 'School', value: 'Caraga State University' },
  { label: 'Nickname', value: 'Kuring' },
]
</script>

<template>
  <div>
    <!-- NAME + INTRODUCTION + PROFILE PICTURE ------------------------------ -->
    <section class="bg-butter px-5 py-14 text-ink md:px-8 md:py-20" aria-labelledby="intro-heading">
      <div class="mx-auto grid max-w-6xl items-center gap-12 md:grid-cols-[1.15fr_1fr] md:gap-16">
        <div>
          <p class="text-xs font-bold uppercase tracking-[0.3em] text-ember">Personal portfolio</p>
          <h1
            id="intro-heading"
            class="mt-3 font-display text-[clamp(1.75rem,3.6vw,2.75rem)] font-black leading-[1.05] tracking-tighter"
          >
            Hi, I'm Leahvenchiteve M. Franco
          </h1>
          <p class="mt-3 font-script text-2xl leading-none text-ember md:text-3xl">you can call me Kuring</p>

          <p class="mt-6 max-w-xl text-base leading-relaxed">
            I am <strong>Leahvenchiteve M. Franco</strong>, an Information Technology student at
            <strong>Caraga State University</strong>. I enjoy learning about technology, solving problems, and exploring
            new experiences. I am continuously working on improving my knowledge, skills, and confidence as I prepare for
            future opportunities.
          </p>

          <dl class="mt-8 grid gap-3 sm:grid-cols-3">
            <div v-for="fact in facts" :key="fact.label" class="rounded-2xl bg-deep px-4 py-3 text-cream">
              <dt class="text-[0.65rem] font-bold uppercase tracking-[0.25em] text-ember">{{ fact.label }}</dt>
              <dd class="mt-1 text-sm font-semibold leading-snug">{{ fact.value }}</dd>
            </div>
          </dl>
        </div>

        <!-- Homepage profile picture (black-and-white portrait) -->
        <div class="relative mx-auto w-full max-w-sm md:max-w-none">
          <div
            class="absolute -left-3 -top-4 z-10 flex items-center gap-1.5 rounded-full bg-deep px-5 py-3 shadow-lg md:-left-8"
            aria-hidden="true"
          >
            <span class="h-2.5 w-2.5 rounded-full bg-butter"></span>
            <span class="h-2.5 w-2.5 rounded-full bg-butter"></span>
            <span class="h-2.5 w-2.5 rounded-full bg-butter"></span>
          </div>
          <img
            src="/images/profile.jpg"
            alt="Black-and-white portrait of Leahvenchiteve M. Franco, also known as Kuring"
            width="828"
            height="608"
            class="aspect-square w-full rounded-[2.5rem] bg-deep object-cover object-center shadow-2xl md:rounded-[3.5rem]"
          />
        </div>
      </div>
    </section>

    <!-- WELCOME MESSAGE ------------------------------------------------------- -->
    <section class="bg-choc px-5 py-14 text-center md:px-8 md:py-20" aria-labelledby="welcome-heading">
      <div class="mx-auto max-w-3xl">
        <p class="font-script text-4xl leading-none text-butter md:text-6xl">Welcome!</p>
        <h2
          id="welcome-heading"
          class="mt-3 font-display text-[clamp(1.75rem,4vw,2.75rem)] font-black leading-[1] tracking-tighter text-ember"
        >
          Thanks for stopping by.
        </h2>
        <p class="mx-auto mt-4 max-w-xl text-base leading-relaxed text-cream/85">
          I'd love for you to know me better. Come explore my skills, interests, and the hobbies that make me, me.
        </p>
        <NuxtLink to="/profile" class="btn-pill btn-ember mt-8">
          Explore My Profile
          <span aria-hidden="true">&rarr;</span>
        </NuxtLink>
      </div>
    </section>
  </div>
</template>
