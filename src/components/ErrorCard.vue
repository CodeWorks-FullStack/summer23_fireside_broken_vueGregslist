<template>
  <div class="error-card alert alert-danger" v-if="error" @click="clear">
    {{ error.message }}
  </div>
</template>


<script>
import { computed } from 'vue';
import { AppState } from '../AppState.js';

export default {
  setup() {
    return {
      error: computed(() => AppState.error),
      clear() {
        AppState.error = null
      }
    }
  }
}
</script>


<style lang="scss" scoped></style>