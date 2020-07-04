<template>
  <div class="about">
    <h1>{{ message }}</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@vue/composition-api";

type Props = {
  message: string;
};

export default defineComponent({
  props: {
    message: {
      type: String,
      default: "default value"
    }
  },
  setup(props: Props) {
    return {
      message: props.message
    };
  }
});
</script>
