<template>
  <div class="question">
    <div class="question-title" @click="isOpen = !isOpen">
      {{ question.title }}
    </div>
    <div class="question-body" v-if="isOpen">{{ question.text }}</div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  props: ['question'],
  setup() {
    const isOpen = ref(false)
    return { isOpen }
  }
}
</script>

<style></style>
