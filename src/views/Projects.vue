<script setup lang="ts">
const projects = [
  {
    title: 'E-commerce Mobile App',
    description: 'Application mobile cross-platform développée avec Flutter',
    technologies: ['Flutter', 'Dart', 'Firebase'],
    image: 'https://placehold.co/600x400',
  },
  {
    title: 'Plateforme de Gestion RH',
    description: 'Application web fullstack avec authentification et tableaux de bord',
    technologies: ['React', 'Node.js', 'Express', 'MongoDB'],
    image: 'https://placehold.co/600x400',
  },
  {
    title: 'API REST pour Blog',
    description: 'API RESTful avec authentification JWT et documentation Swagger',
    technologies: ['NestJS', 'TypeScript', 'PostgreSQL'],
    image: 'https://placehold.co/600x400',
  },
]
</script>

<template>
  <div class="section-container">
    <h1 class="section-title">Mes Projets</h1>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div v-for="project in projects" :key="project.title" class="card">
        <img :src="project.image" :alt="project.title" class="w-full h-48 object-cover rounded-lg mb-4">
        <h3 class="text-xl font-semibold text-gray-900 mb-2">{{ project.title }}</h3>
        <p class="text-gray-600 mb-4">{{ project.description }}</p>
        <div class="flex flex-wrap gap-2">
          <span 
            v-for="tech in project.technologies" 
            :key="tech"
            class="px-3 py-1 bg-primary/10 text-primary rounded-full text-sm"
          >
            {{ tech }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>