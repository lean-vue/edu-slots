<template>
  <div class="flex justify-center text-center mt-8">
    <div class="flex flex-col gap-y-4 w-32">
      <app-button type="button">Click mich!</app-button>
      <app-button type="button" variant="outline">Secondary</app-button>
      <app-button type="button" variant="danger">Attention</app-button>
    </div>
  </div>
</template>

<script>
import AppButton from '../lib/AppButton.vue';
export default {
  components: { AppButton },
};
</script>
