<script setup>
import fs from "fs"; // nao funciona pois vue é csr, somente em ssr
import fsx from "file-saver";

function outFile() {
  const txt = document.querySelector("#txtarea").value;
  /*   fs.appendFile("output.txt", txt, (error) => {
    if (error) throw error;
    console.log("saved");
  }); */
  const blob = new Blob([txt], { type: "text/plain;charset=utf-8" });
  fsx.saveAs(blob, 'out.txt')

  console.log(txt);
}
</script>

<template>
  <div>
    <h1>hi</h1>
    <textarea id="txtarea"></textarea>
    <button @click="outFile">ok</button>
  </div>
</template>

<style scoped>
</style>
