<template>
  <div class="icon-wrapper">
    <ThankYouIcon />
    <p>You selected {{ rating }} out 5</p>
    <div class="thanks">
      <h1>Thank you!</h1>
      <span>
        We appreciate you taking the time to give a rating. If you ever need
        more support don't hesitate to get in touch!
      </span>
    </div>
  </div>
</template>

<script setup lang="ts">
import ThankYouIcon from "../../icons/thankYouIcon.vue";
interface Props {
  rating: number;
}

defineProps<Props>();
</script>

<style scoped>
.icon-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

p {
  color: hsl(25, 97%, 53%);
  background: hsl(213, 19%, 18%);
  padding: 0.5rem;
  border-radius: 2rem;
}
.thanks {
  margin: 0;
  text-align: center;
}

.thanks h1 {
  color: white;
}

.thanks span {
  color: hsl(216, 12%, 54%);
}
</style>
