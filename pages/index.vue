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

<style scoped>
  .home {
    padding: 92px 30px 30px;
    text-align: center;
  }

  .home-title {
    font-size: 37px;
    letter-spacing: -1.5px;
    margin-bottom: 45px;
    position: relative;
  }

  .home-title::after {
    background-color: var(--white);
    content: '';
    height: 2px;
    margin-top: 16px;
    position: absolute;
    right: 50%;
    top: 100%;
    transform: translateX(50%);
    width: 32px;
  }

  .home-description {
    margin: 0 auto 47px;
    max-width: 700px;
  }

  .home-blocks {
    column-gap: 30px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    max-width: 1506px;
    margin: 0 auto;
  }

  @media(max-width: 1280px) {
    .home-blocks {
      column-gap: 24px;
      grid-template-columns: repeat(3, 1fr);
    }
  }

  @media(max-width: 768px) {
    .home-blocks {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  @media(max-width: 600px) {
    .home-blocks {
      grid-template-columns: repeat(1, 1fr);
    }
  }
</style>
