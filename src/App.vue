<script setup>
import Note from "./components/Note.vue";
</script>

<template>
  <div class="nav">nav</div>
  <div class="container">
    <Note />
  </div>
  <div class="footer">foot</div>
</template>

<style>
* {
  margin: 0 auto;
  padding: 0;
}

.container {
  display: flex;
  height: 100vh;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}

.nav {
  background-color: black;
  height: 80px;
}

.footer {
  background-color: black;
  height: 80px;
}
</style>
