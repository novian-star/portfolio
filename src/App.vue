<script setup lang="ts">
import { Printer } from 'lucide-vue-next';
import FirstPage from './components/pages/FirstPage.vue';
import SecondPage from './components/pages/SecondPage.vue';

function handlePrint() {
  window.print();
}
</script>

<template>
  <main class="relative w-screen h-screen">
    <!-- Portfolio container -->
    <section
      class="flex flex-col md:items-center p-8 print:p-0 gap-8 overflow-auto print:gap-0"
    >
      <FirstPage />

      <SecondPage />
    </section>

    <!-- Print button -->
    <div class="fixed bottom-0 w-auto p-4 print:hidden">
      <div class="flex justify-end max-w-4xl mx-auto">
        <button
          class="flex items-center p-2 gap-2 bg-emerald-500 rounded shadow text-sm"
          @click="handlePrint"
        >
          <Printer class="w-6 h-6 !text-white" color="white" />
        </button>
      </div>
    </div>
  </main>
</template>
