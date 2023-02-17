<template>
  <button
    class="vk-button"
    :class="{
      [`vk-button--${type}`]: type,
      [`vk-button--${size}`]: size,
      'is-plain': plain,
      'is-round': round,
      'is-circle': circle,
      'is-disabled': disabled,
    }"
    :disabled="disabled"
  >
    <span>
      <slot />
    </span>
  </button>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'VkButton'
})
</script>
<script setup lang="ts">
// import type { ButtonProps } from './types'
import { buttonProps } from './types'
defineProps(buttonProps)
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
