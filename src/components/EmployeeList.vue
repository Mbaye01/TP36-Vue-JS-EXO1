<!-- <template>
 <h1>EXO 1 VUE JS TP 38 </h1>
</template>

<script>

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style> -->
<template>
  <div>
    <h2>Liste des employés</h2>
    <ol>
      <li v-for="employee in employees" :key="employee.id" @mouseover="hover = employee.id" @mouseleave="hover = null" :class="{ hover: hover === employee.id }">
        {{ employee.name }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: null,
      employees: [
        { id: 1, name: 'Ibrahima' },
        { id: 2, name: 'Bocar' },
        { id: 3, name: 'Ousmane' }
      ]
    };
  }
};
</script>

<style scoped>
ol {
  padding: 0;
  list-style: none;
}

li {
  padding: 10px;
  margin: 5px 0;
  background-color: #f0f0f0;
  cursor: pointer;
}

.hover {
  background-color: rgb(31, 141, 31);
}
h2{
  color : green;
}
</style>

