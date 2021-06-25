<template>
  <div class="border rounded border-gray-300">
    <div class="p-4 border-b border-gray-300">
      <slot name="header"></slot>
    </div>
    <div class="p-4">
      <slot />
    </div>
    <div class="bg-gray-100 p-4">
      <slot name="footer"></slot>
    </div>
  </div>
</template>
