<script setup>
import fs from "fs"; // nao funciona pois vue é csr, somente em ssr
import fsx from "file-saver";

function outFile() {
  const txt = document.querySelector("#txtarea").value;

  const blob = new Blob([txt], { type: "text/plain;charset=utf-8" });
  fsx.saveAs(blob, "out.txt");

  console.log(txt);
}
</script>

<template>
  <div class="card">
    <h1>WEBNote</h1>
    <!-- <p>words enter book</p> -->
    <textarea id="txtarea" rows="4" cols="14" maxlength="500"></textarea>
    <div class="btn" @click="outFile">export file</div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 25px;
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  max-width: 1200px;
  min-width: 800px;

}

.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgb(168, 215, 121);
  color: black;
  height: 30px;
  width: 100px;
  border-radius: 20px;
  cursor: pointer;
}
.btn:hover {
  background-color: rgb(152, 196, 108);
}

#txtarea {
  max-height: 550px;
  max-width: 900px;
  min-height: 550px;
  min-width: 150px;
  width: 900px;
  border: 2px solid #ccc;
  border-radius: 8px;
  padding: 8px;
  font-size: 16px;
  resize: horizontal;

  -webkit-box-shadow: 0px 9px 8px 3px #000000;
  box-shadow: 0px 9px 8px 3px #000000;
}
</style>
