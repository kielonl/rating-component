<template>
  <main role="main">
    <div class="container">
      <RatingForm
        :setRating="setRating"
        :rating="rating"
        :submit="handleSubmit"
        v-if="submitted === false"
      />
      <RatingSubmitted :rating="rating" v-else />
    </div>
  </main>
</template>

<script setup lang="ts">
import RatingForm from "./ratingForm.vue";
import RatingSubmitted from "./ratingSubmitted.vue";
import { ref } from "vue";

const rating = ref<number>(0);
const submitted = ref<boolean>(false);

const setRating = (value: number) => {
  rating.value = value;
};

const handleSubmit = () => {
  submitted.value = true;
};
</script>

<style>
@import url("./rating.css");
@import url("https://fonts.google.com/specimen/Overpass");
* {
  font-family: "Overpass", sans-serif;
}
</style>
