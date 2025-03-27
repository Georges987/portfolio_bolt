<script setup lang="ts">
const technologies = [
  { name: 'Frontend', items: ['React.js', 'Vue.js', 'Next.js', 'Nuxt.js'] },
  { name: 'Mobile', items: ['Flutter', 'React Native'] },
  { name: 'Backend', items: ['Laravel', 'Express.js', 'NestJS', 'Django', 'Flask', 'Ruby on Rails'] },
  { name: 'Languages', items: ['JavaScript', 'TypeScript', 'Python', 'PHP', 'C/C++', 'Dart'] },
]
</script>

<template>
  <div>
    <!-- Hero Section -->
    <section class="bg-gradient-to-r from-primary to-secondary text-white">
      <div class="section-container">
        <div class="max-w-3xl mx-auto text-center">
          <h1 class="text-4xl sm:text-6xl font-bold mb-6">
            Développeur Fullstack Web & Mobile
          </h1>
          <p class="text-xl mb-8">
            Passionné par la création d'applications performantes et innovantes
          </p>
          <div class="flex justify-center space-x-4">
            <router-link to="/projects" class="btn-primary">
              Voir mes projets
            </router-link>
            <router-link to="/contact" class="bg-white text-primary px-6 py-2 rounded-lg hover:bg-gray-100 transition-colors duration-300">
              Me contacter
            </router-link>
          </div>
        </div>
      </div>
    </section>

    <!-- Technologies Section -->
    <section class="bg-white">
      <div class="section-container">
        <h2 class="section-title">Technologies Maîtrisées</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div v-for="tech in technologies" :key="tech.name" class="card">
            <h3 class="text-xl font-semibold mb-4 text-primary">{{ tech.name }}</h3>
            <ul class="space-y-2">
              <li v-for="item in tech.items" :key="item" class="text-gray-700">
                {{ item }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="bg-gray-50">
      <div class="section-container">
        <div class="max-w-3xl mx-auto text-center">
          <h2 class="section-title">À Propos</h2>
          <p class="text-lg text-gray-700 mb-6">
            Je suis un développeur fullstack passionné par la création d'applications web et mobiles innovantes.
            Avec une expertise approfondie dans de nombreuses technologies modernes, je peux transformer vos idées en solutions concrètes.
          </p>
          <p class="text-lg text-gray-700">
            Mon approche combine créativité, performance et qualité pour délivrer des applications qui répondent parfaitement aux besoins des utilisateurs.
          </p>
        </div>
      </div>
    </section>
  </div>
</template>