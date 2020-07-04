<template>
  <div class="flex flex-col h-screen">
    <Navbar />
    <router-view />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";
import Navbar from "@/components/Navbar.vue";

export default defineComponent({
  components: {
    Navbar
  }
});
</script>

<style></style>
