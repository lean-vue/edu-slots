<template>
  <div class="min-h-screen flex flex-col items-center gap-y-8 mt-8">
    <h1 class="text-3xl font-semibold">Slots</h1>
    <div class="w-full">
      <nav class="flex justify-center text-gray-500">
        <div class="flex-shrink flex gap-x-8 border-b-2 border-gray-200 px-8">
          <a
            v-for="(tab, index) in tabs"
            :key="index"
            href="#"
            class="translate-y-[2px] px-4"
            :class="
              activeTab === tab ? 'text-black border-b-2 border-indigo-500' : ''
            "
            @click.prevent="activeTab = tab"
          >
            {{ tab.title }}
          </a>
        </div>
      </nav>
      <div class="w-3/4 mx-auto pt-4">
        <component :is="activeTab.component" />
      </div>
    </div>
  </div>
</template>

<script>
import { shallowRef } from 'vue';
import NamedSlotTab from './components/NamedSlotTab.vue';
import SlotContentTab from './components/SlotContentTab.vue';

const tabs = [
  { title: 'Slot Content', component: SlotContentTab },
  { title: 'Named Slots', component: NamedSlotTab },
];

export default {
  name: 'App',
  setup() {
    const activeTab = shallowRef(tabs[0]);
    return {
      tabs,
      activeTab,
    };
  },
};
</script>
