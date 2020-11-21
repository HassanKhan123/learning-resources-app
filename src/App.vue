<template>
  <ul>
    <LearningResources
      v-for="storedResource in storedResources"
      :key="storedResource.id"
      :id="storedResource.id"
      :title="storedResource.title"
      :description="storedResource.description"
      :link="storedResource.link"
    />
  </ul>
</template>

<script>
import LearningResources from './components/learning-resources/LearningResource';

export default {
  components: {
    LearningResources,
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The official Vue js documentation',
          link: 'https://vuejs.org',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn how to google..',
          link: 'https://google.com',
        },
      ],
    };
  },
};
</script>