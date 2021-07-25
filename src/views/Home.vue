<template>
  <v-container>
    <v-layout align-center justify-space-around column fill-height wrap class="my-5 text-center">
      <h1
        class="my-3 font-weight-thin white--text my-5"
      >به سرویس نمایش  فیلم وسریال وینما خوش آمدید</h1>

      <v-img contain width="50vw" height="50vh" src="../assets/undraw_horror_movie.svg"></v-img>

      <v-btn color="primary" min-width="200" class="my-5" router to="/movies-playing-now">گشت و گذار</v-btn>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    components: {},
    data() {
      return {};
    }
  };
</script>

<style>
</style>
