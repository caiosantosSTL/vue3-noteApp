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
  <div class="container">
    <h1>WEBNote</h1>
    <div class="card">
      <!-- <p>words enter book</p> -->
      <textarea id="txtarea" rows="4" cols="14" maxlength="500"></textarea>

    </div>
    <div class="btn" @click="outFile">export file</div>
  </div>
</template>

<style scoped>
.container {
  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  gap: 25px;

}
.card {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  height: 800px;
  width: 900px;
  min-width: 200px;
  /* background-color: rgb(205, 90, 90); */
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
  height: 100%;
  width: 100%;
  border: 2px solid #ccc;
  border-radius: 8px;
  padding: 8px;
  font-size: 16px;
  resize: none;

  -webkit-box-shadow: 0px 9px 8px 3px #000000;
  box-shadow: 0px 9px 8px 3px #000000;
}
</style>
