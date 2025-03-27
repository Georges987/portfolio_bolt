<script setup lang="ts">
const skills = [
  {
    category: 'Frontend',
    items: [
      { name: 'React.js', level: 90 },
      { name: 'Vue.js', level: 85 },
      { name: 'Next.js', level: 80 },
      { name: 'Nuxt.js', level: 75 },
    ]
  },
  {
    category: 'Mobile',
    items: [
      { name: 'Flutter', level: 85 },
      { name: 'React Native', level: 80 },
    ]
  },
  {
    category: 'Backend',
    items: [
      { name: 'Laravel', level: 90 },
      { name: 'Express.js', level: 85 },
      { name: 'NestJS', level: 80 },
      { name: 'Django', level: 75 },
      { name: 'Flask', level: 70 },
      { name: 'Ruby on Rails', level: 65 },
    ]
  },
  {
    category: 'Languages',
    items: [
      { name: 'JavaScript', level: 95 },
      { name: 'TypeScript', level: 90 },
      { name: 'Python', level: 85 },
      { name: 'PHP', level: 85 },
      { name: 'C/C++', level: 75 },
      { name: 'Dart', level: 80 },
    ]
  },
]
</script>

<template>
  <div class="section-container">
    <h1 class="section-title">Compétences Techniques</h1>
    <div class="space-y-12">
      <div v-for="category in skills" :key="category.category" class="card">
        <h2 class="text-2xl font-semibold text-primary mb-6">{{ category.category }}</h2>
        <div class="space-y-4">
          <div v-for="skill in category.items" :key="skill.name" class="space-y-2">
            <div class="flex justify-between items-center">
              <span class="text-gray-700">{{ skill.name }}</span>
              <span class="text-primary font-medium">{{ skill.level }}%</span>
            </div>
            <div class="h-2 bg-gray-200 rounded-full">
              <div 
                class="h-full bg-primary rounded-full transition-all duration-500"
                :style="{ width: `${skill.level}%` }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>