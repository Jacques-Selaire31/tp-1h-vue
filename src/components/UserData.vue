<template>
    <div class="form">
        <label for="name">Nom:</label>
        <input v-model="name" type="text" placeholder="Entrer un nom" class="input input-primary" />
        <label for="age">Age:</label>
        <input v-model="age" type="number" placeholder="Entrer votre age" class="input input-primary" />
        <button @click="pushUserToDisplay" class="btn btn-secondary">Mettre à jour</button>
    </div>

</template>
<script setup>
import { ref } from 'vue';
const name = ref("");
const age = ref();
console.log(name, age);
const emit = defineEmits(["add-user"]);
const pushUserToDisplay = () => {
    emit("add-user", name.value, age.value);
    console.log(name.value, age.value);
}

</script>
<style scoped>
.form {
    display: flex;
    flex-direction: column;
    padding: 15px;
    margin: 15px;
}
</style>
