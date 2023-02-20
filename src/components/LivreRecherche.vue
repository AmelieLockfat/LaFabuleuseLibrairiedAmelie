<script setup>
import { defineEmits, ref } from "vue";
import Livre from "../Livre.js";
const emit = defineEmits(["searchL"]);
</script>

<template>
  <h3><img src="../assets/loupe.png"/>Recherche de livres dans la librairie :</h3>
  <form @submit.prevent="$emit('searchL', recherche)">
    <input type="text" v-model="recherche" placeholder="titre ou mot clé?" />
    <input type="submit" value="Valider" />
  </form>
  <p><ul id="listeTrouve"></ul></p>
</template>

<style >
input {
  background-color: rgb(234, 173, 173);
  color: black;
  border-color: black;
  font-family: "Comic Sans MS";
}
</style>