<template>
  <div>
    <h4>Skills</h4>
    <div class="container">
      <ul>
        <li v-for="skill in skills" :key="skill.name">
          <el-tag type="warning" size="mini" effect="dark">{{
            skill.name
          }}</el-tag>
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
          name: 'Proactive'
        },
        {
          name: 'Creative'
        },
        {
          name: 'Self-efficient'
        },
        {
          name: 'Love to code'
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
  grid-template-columns: 1fr;
  margin: 5px;
}
h4 {
  color: var(--gray);
  text-align: center;
  margin-bottom: 0;
}
</style>
