<template>
  <div class="block">
    <div class="block-header">
      i
      <!-- <img class="block-icon" /> -->
    </div>

    <div class="block-body">
      <h2 class="block-title">{{ title }}</h2>
      <p class="block-description" :class="{ active: isActive }">
        {{ description }}
      </p>
      <button class="block-toggle" :class="{ active: isActive }">
        +
        <!-- <img src="" alt=""> -->
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
