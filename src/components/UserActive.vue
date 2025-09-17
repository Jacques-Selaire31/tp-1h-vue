<template>
  <div class="display-user">

    <h1>Composant affichage des données utilisateurs</h1>
    <p v-for="user in users" :name="user.name" :age="user.age"></p>
  </div>
  <UserData @add-user="DisplayUser" />
</template>

<script setup lang='js'>
import { computed, watch, onMounted, onUpdated, onBeforeUnmount, ref } from 'vue'
import UserData from './UserData.vue';


const users = ref([{ name: "John", age: 25 }]);

const DisplayUser = () => {
  users.value.push({ name: name.value, age: age.value });
  console.log(users);
}


</script>
<style scoped lang="css"></style>