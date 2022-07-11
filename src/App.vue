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
  margin: 0 ;
  padding: 0;
}
.aa{
  background-color: aqua;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 900px;
  min-width: 200px;
}
textarea{
  width: 100%;
  resize: none;
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
