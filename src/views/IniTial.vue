<template>
  <div class="bar">
    <h3>FORMULÁRIO</h3>
  </div>
  <div class="container">
    <div class="image">
      <img src="../assets/Fer.png" alt="Fernanda" />
    </div>
    <div v-show="Fase1">
    <FormuLario />
    </div>
  </div>
</template>

<script>
import FormuLario from '../components/FormuLario.vue'

export default {
  name: "IniTial",
  components: {
    FormuLario
  },
  data() {
    return {
      Fase1: true
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row-reverse;
}

img {
  width: 400px;
}

.bar {
  background-color: #e02b57;
  padding: 10px;
  align-items: center;
  color: white;
}
</style>
