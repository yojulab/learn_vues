<template>
  <!-- template : div elements 사용 시 <div>가 <ul> 안에 남음. -->
  <ul>
    <div v-if="!isActive">
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </div>
    <template v-else>
      <li>Item 4</li>
      <li>Item 5</li>
      <li>Item 6</li>
    </template>
  </ul>
  <!-- v-show - stype="display: none;" -->
  <h2 v-show="!isActive">Hello World</h2>
  <h2 v-if="!isActive">Hello World</h2>

  <!-- v-if -->
  <h2 v-if="isActive">Hello World</h2>
  <h2 v-else>Goodbye World</h2>
  <h2 v-if="user.age > 18">Adult {{ user.name }}</h2>
  <h2 v-else-if="user.age > 14">Teenager {{ user.name }}</h2>
  <h2 v-else>Child {{ user.name }}</h2>
  <input v-model="user.age" />

  <!-- v-once -->
  <input type="text" name="" id="" v-model="message" />
  <!-- Try Change Text -->
  <h2 v-once>Hello {{ message }}</h2>
  <h2>{{ message }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      message: "Welcome to Your Vue.js",
      isActive: false,
      user: {
        name: "John Doe",
        age: 30,
      },
    };
  },
  // components: {
  //   HelloWorld
  // }
};
</script>

<style></style>
