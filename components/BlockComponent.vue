<template>
  <div class="block">
    <div class="block-header">
      <img class="block-icon" srcset="~/assets/icon-i_2x.png 2x" src="~/assets/icon-i.png"/>
    </div>

    <div class="block-body">
      <h2 class="block-title">{{ title }}</h2>
      <p class="block-description" :class="{ active: isActive }">
        {{ description }}
      </p>
      <button class="block-toggle" :class="{ active: isActive }">
        <img src="" alt="">
        <img srcset="~/assets/icon-plus_2x.png 2x" src="~/assets/icon-plus.png"/>
        <!-- <img srcset="~/assets/icon-minus_2x.png 2x" src="~/assets/icon-minus.png"/> -->
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlockComponent',
  props: {
    title: { type: String, required: true },
    description: { type: String, required: true },
  },
  data: () => ({
    isActive: false,
  }),
  methods: {
    toggle() {
      this.isActive = !this.isActive
    },
  },
}
</script>

<style scoped>
  .block {
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    margin-bottom: 31px;
    overflow: hidden;
  }

  .block-header {
    background-color: var(--green);
    padding: 32px 0 20px;
  }

  .block-body {
    background-color: var(--black);
    padding: 26px 15px 18px;
  }

  .block-title {
    font-size: 15px;
    margin-bottom: 10px;
    text-transform: uppercase;
  }

  .block-description {
    height: 2.5em;
    margin: 0 auto 14px;
    max-width: 230px;
    overflow: hidden;
  }

  .block-toggle {
    align-items: center;
    appearance: none;
    background-color: var(--gray-dark);
    border-radius: 100%;
    border: none;
    display: flex;
    height: 34px;
    justify-content: center;
    margin: 0 auto;
    padding: 0;
    width: 34px;
  }
</style>
