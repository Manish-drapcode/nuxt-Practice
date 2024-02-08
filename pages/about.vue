<script setup="js">
const [firstName, firstNameModifiers] = defineModel("firstName");
const [lastName, lastNameModifiers] = defineModel("lastName");
const awesome = ref(true);
function dosomestuff() {
  console.log("hello");
}
// { uppercase: true}
</script>

<template>
  <div class="container bg-dark text-white">
    <div class="card">
      <p>Name:</p>
      <input type="text" v-model="firstName" />
      <p>email</p>
      <input type="text" v-model="lastName" /><br />

      <div>
        <button @click="awesome = !awesome">Toggle</button>
        <br />
        <h1 v-if="awesome">{{ firstName }}</h1>
        <h1 v-else>Oh no 😢</h1>
      </div>
    </div>
  </div>
</template>
