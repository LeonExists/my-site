<script setup>
import Project from './Project.vue'

const projects = [
    {
        title: 'Project 1',
        description: 'This is the first project.',
        tags: ['Vue', 'JavaScript'],
        source: 'https://github.com/',
        link: 'https://youtube.com/',
    },
]
</script>

<template>
    <section>
        <h2>Projects</h2>

        <div class="projects">
            <Project
                v-for="project in projects"
                :key="project.title"
                :title="project.title"
                :description="project.description"
                :tags="project.tags"
                :source="project.source"
                :link="project.link"
            />
        </div>
    </section>
</template>

<style scoped>
.projects {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1rem;

    margin-top: 1rem;
}
</style>