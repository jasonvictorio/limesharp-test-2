<template>
  <div class="home">
    <div class="home-header">
      <h1 class="home-title">{{ title }}</h1>
      <p class="home-description">{{ description }}</p>
    </div>
    <div class="home-blocks">
      <block-component
        v-for="block in blocks"
        :key="block.title"
        :title="block.title"
        :description="block.description"
      ></block-component>
    </div>
  </div>
</template>

<script>
import BlockComponent from '~/components/BlockComponent.vue'

export default {
  name: 'IndexPage',
  components: { BlockComponent },
  data: () => ({
    title: 'Experienced & Multi-Talented',
    description:
      'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam tortor leo, portitor vel dictum at, aliquam et augeue. Duis vel molestie risus, ut lobortis felis.',
    blocks: [
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
      {
        title: 'Block',
        description:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut vestibulum eros nisi, eu sagit-tis nisl feugiat quis.',
      },
    ],
  }),
}
</script>
