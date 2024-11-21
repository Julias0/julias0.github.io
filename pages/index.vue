<script setup lang="ts">
useHead({
  title: 'Dhar\'s website',
  meta: [
    { name: 'description', content: 'Welcome to my blog!. This will be the container of my learnings, articles and whatnot.' }
  ],
  bodyAttrs: {
  },
  script: []
})
</script>

<template>
  <main class="bg-white text-black antialiased text-dark">
    <div class="mx-10 pb-8 pt-6 md:space-y-5">
      <h1
        class="text-2xl font-extrabold leading-9 tracking-tight text-dark sm:text-4xl sm:leading-10 md:text-5xl md:leading-14">
        Hi! I'm <span
          class="from-secondary-700 to-secondary-400 mt-10 ml-1 bg-clip-text text-center text-4xl font-extrabold tracking-tight sm:text-5xl lg:text-6xl">Dhar</span>

        <!-- -->👋</h1>
      <div class="text-grey text-black mb-8  mt-4 text-base">
        <ContentDoc />

        <p class="text-grey text-black mb-8   mt-4 text-sm">
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🛠️ Javascript</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🥇 Nuxt.js</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🤖 OpenAI API</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">📦 NodeJS</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">⏳ Angular</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🧊 HTML</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🍡 CSS</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🕰️ Git</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🚃 Npm</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🧶 Yarn</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">📜 MongoDB</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">📃 Postgres</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🎢 Redux</span>
          <span class="mr-3 inline-block whitespace-nowrap pt-3">🍽️ APIs</span>
        </p>
      </div>

      <p class="text-lg leading-7 text-black">My chatter about life and the tech realm</p>

      <ContentList path="/articles" v-slot="{ list }">
        <div v-for="article in list" :key="article._path">
          <article>
            <div class="space-y-2 xl:grid xl:grid-cols-4 xl:items-baseline xl:space-y-0">
              <div class="space-y-5 xl:col-span-3">
                <div class="space-y-6">
                  <div>
                    <h2 class="text-2xl font-bold leading-8 tracking-tight"><a class="text-black-900"
                        v-bind:href="article._path">{{ article.title }}</a></h2>
                  </div>
                  <div class="prose max-w-none text-black-500">
                    {{ article.description }}
                  </div>
                </div>
                <div class="text-base font-medium leading-6"><a
                    class="text-primary-500 hover:text-primary-600 dark:hover:text-primary-400"
                    v-bind:href="article._path">Read more
                    →</a></div>
              </div>
            </div>
          </article>
        </div>
      </ContentList>
    </div>
  </main>
</template>