<script setup>
defineProps({
    title: String,
    description: String,
    tags: Array,
    source: String,
    link: String
})
</script>

<template>
    <div class="project">
        <h2 class="title">{{ title }}</h2>
        <p class="description">{{ description }}</p>

        <div class="tags">
            <span v-for="tag in tags" :key="tag" class="tag">{{ tag }}</span>
        </div>

        <div class="links">
            <a :href=source target="_blank" class="link">GitHub ↗</a>
            <a :href=link target="_blank" class="link">View ↗</a>
        </div>
    </div>
</template>

<style scoped>
.project {
    padding: 1.5rem;

    background-color: var(--color-card);
    
    border: 1px solid var(--color-border);
    border-radius: 8px;

    transition: transform 0.1s ease;
}
.project:hover {
    transform: scale(1.02) translateY(-6px);
}


/* Title */
.title {
    font-size: 1.5rem;
    font-weight: 600;
}

/* Description */
.description {
    margin-top: 0.5rem;

    color: var(--color-text);
    font-size: 1rem;
    line-height: 1.5;
}

/* Tags */
.tags {
    margin-top: 0.5rem;
    display: flex;
    gap: 0.5rem;
}

.tag {
    padding: 2px 8px;

    background-color: var(--color-tag);

    /* border: 1px solid var(--color-border); */
    border-radius: 2px;

    font-size: 0.875rem;
}


/* Links */
.links {
    margin-top: 1rem;
    display: flex;
    gap: 1rem;

    padding-top: 1rem;
    
    border-top: 1px solid var(--color-border);
}

.link {
    font-weight: 500;

    transition: transform 0.1s ease;
}
.link:hover {
    transform: translateY(-2px);
}


</style>