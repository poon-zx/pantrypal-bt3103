<template>
  <aside class="sidebar">
    <div class="menu-container">
      <img src="../assets/recipe-generator-map.png" height="500px"/>
      <div class="header" :class="{ selected: selected === 'input' }">
        <h3>Input Leftovers</h3>
      </div>
      <div class="header" :class="{ selected: selected === 'generate' }">
        <h3>Generate Recipe</h3>
      </div>
      <div class="header save" :class="{ selected: selected === 'save' }">
        <h3>Save Recipe</h3>
      </div>
      <div>
        <h3>And Start Cooking!</h3>
      </div>
    </div>
  </aside>
</template>
<script>
export default {
  name: "Recipe Generator Sidebar",
  props: {
    selected: String,
  },
};
</script>

<style scoped>
.sidebar {
  background-color: #3c1f11;
  min-width: 12rem;
  padding: 1rem;
  display: flex;
  justify-content: center;
  text-align: center;
  position: sticky;
  height: 95.9vh;
  top: 0;
  overflow-y: hidden;
  padding-top: 70px;
}

.menu-container {
  padding-top: 5rem;
  height: fit-content;
  position: relative;
}

.header {
  margin-bottom: 6.5rem;
}

.save {
  margin-bottom: 10rem;
}

h3 {
  color: #a7bf6a;
  margin: 0 auto;
  padding: 5px 0px;
}

.selected h3 {
  background-color: #a7bf6a;
  width: 100%;
  padding: 5px 5px;
  border-radius: 16px;
  color: #3c1f11;
}

img {
  position: absolute;
  top: 85px;
  left: -30px;
  z-index: 1;
}
</style>
