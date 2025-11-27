<template>
  <div class="display-user">
    <h3>Composant affichage des données utilisateurs</h3>
    <p>{{ name }}</p>
    <p>{{ age }}</p>
  </div>
</template>

<script setup lang='js'>

const props = defineProps({
  name: {
    type: String,
    required: true,
  },
  age: {
    type: Number,
    required: true,
  },
})

</script>
<style scoped lang="css">
.display-user {
  width: 300px;
  background-color: blue;
  border-radius: 25px;
  padding: 15px;
  margin: 15px;
}
</style>