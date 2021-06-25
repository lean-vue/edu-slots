<template>
  <button
    :class="variantClass"
    class="
      inline-flex
      justify-center
      py-2
      px-4
      border border-transparent
      shadow-sm
      text-base
      font-medium
      rounded-md
      focus:outline-none focus:ring-2 focus:ring-offset-2
    "
  >
    <slot />
  </button>
</template>

<script>
import { ref } from 'vue';
const variantStyles = {
  default: 'text-white bg-indigo-600 hover:bg-indigo-700 focus:ring-indigo-500',
  danger: 'text-white bg-red-600 hover:bg-red-700 focus:ring-red-500',
  outline:
    'text-gray-700 bg-white hover:bg-gray-50 focus:ring-indigo-500 border-gray-300',
};

export default {
  props: {
    variant: {
      type: String,
      default: 'default',
    },
  },
  setup(props) {
    const variantClass = ref(variantStyles[props.variant]);

    return {
      variantClass,
    };
  },
};
</script>
