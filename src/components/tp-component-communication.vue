<template>
    <div class="component-user">
        <h1>Composant Gestion de l'utilisateur</h1>
            <UserActive :name="user.name" :age="user.age"></UserActive>
            <UserData @add-user="refreshUserData"></UserData>
    </div>
</template>

<script setup lang='js'>
import UserActive from './UserActive.vue';
import UserData from './UserData.vue';
import { ref } from 'vue';

const user = ref({
    name : "John",
    age : 30
})

const refreshUserData = (newName, newAge) => {
    user.value = {
        name: newName,
        age : newAge
    }
}
</script>

<style>
.component-user{
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>