<script setup>
import { useStoryblok } from '@storyblok/vue';
const story = await useStoryblok('home', { version: 'published' });
</script>

<template>
  <div v-if="story">
    <StoryblokComponent :blok="story.content" />
  </div>
</template>