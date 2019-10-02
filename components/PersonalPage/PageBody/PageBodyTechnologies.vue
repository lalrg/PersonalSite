<template>
  <div>
    <h4>Technologies</h4>
    <div class="container">
      <ul>
        <li v-for="skill in skills" :key="skill.name">
          {{ skill.name }}
          <el-progress
            :percentage="skill.percentage"
            :color="`var(--${skill.color})`"
          ></el-progress>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  data: () => {
    return {
      skills: [
        {
          name: 'Dotnet',
          percentage: 90,
          color: 'green'
        },
        {
          name: 'VueJs',
          percentage: 60,
          color: 'green'
        },
        {
          name: 'MSSQL',
          percentage: 50,
          color: 'green'
        },
        {
          name: 'React',
          percentage: 20,
          color: 'green'
        },
        {
          name: 'Microsoft Azure',
          percentage: 90,
          color: 'green'
        }
      ]
    }
  }
}
</script>
<style scoped>
ul {
  list-style-type: none;
}
.container {
  display: grid;
  align-content: center;
  align-items: center;
}
li {
  display: grid;
  grid-template-columns: 1fr 4fr;
  grid-column-gap: 15px;
}
h4 {
  color: var(--gray);
  text-align: center;
  margin-bottom: 0;
}
</style>
