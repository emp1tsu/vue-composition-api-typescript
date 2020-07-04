<template>
  <div class="flex flex-1 h-full">
    <nav class="bg-gray-400 w-64">
      <p>サイドバー</p>
    </nav>
    <main class="bg-gray-100 flex w-full">
      <div>メイン</div>
      <button @click="increment">
        Count is: {{ state.count }}, double is: {{ state.double }}
      </button>
    </main>
  </div>
</template>

<script>
import { reactive, computed, defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {
    const state = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    });

    function increment() {
      state.count++;
    }

    return {
      state,
      increment
    };
  }
});
</script>
