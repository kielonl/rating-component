<template>
  <StarIcon />
  <form @submit="submit">
    <h2>How did we do?</h2>
    <p>
      Please let us know how we did with your support request. All feedback is
      appreciated to us improve our offering
    </p>
    <div class="rating">
      <button
        type="button"
        class="rating-button"
        :class="rating === button && 'selected'"
        v-for="button in [1, 2, 3, 4, 5]"
        v-bind:key="button"
        @click="setRating(button)"
      >
        {{ button }}
      </button>
    </div>
    <div class="submit">
      <button type="submit" class="submit-button">SUBMIT</button>
    </div>
  </form>
</template>

<script setup lang="ts">
import { ref } from "vue";
import StarIcon from "../../icons/starIcon.vue";

interface Props {
  rating: number;
  setRating: (value: number) => void;
  submit: () => void;
}

defineProps<Props>();
</script>
