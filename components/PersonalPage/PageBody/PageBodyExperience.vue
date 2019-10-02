<template>
  <div class="block">
    <el-timeline>
      <el-timeline-item
        v-for="(experience, index) in experiences"
        :key="index"
        :timestamp="`${experience.startDate} - ${experience.endDate}`"
        placement="top"
      >
        <el-card>
          <h3 class="text">{{ experience.role }}</h3>
          <h4 class="text">{{ experience.company }}</h4>
          <p class="text">{{ experience.description }}</p>
          <ul>
            <li
              v-for="(technology,
              techIndex) in experience.implementedTechnologies"
              :key="techIndex"
            >
              <p class="text">
                <b>{{ technology.name }}</b
                >: {{ technology.workDone }}
              </p>
            </li>
          </ul>
        </el-card>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script>
export default {
  data() {
    return {
      experiences: [
        {
          startDate: '2016/02/02',
          endDate: '2018/05/17',
          role: 'Software developer',
          company: 'Datasoft Netsolutions',
          description:
            "On this job, I visited many clients on their locations inside Costa Rica, understanding their requirements and giving them the best possible solution based on the team's skills and client's budget and infraestructure.",
          implementedTechnologies: [
            {
              name: 'TFS',
              workDone:
                "Almost all the applications's source code was controlled by TFS"
            },
            {
              name: 'Microsoft Azure',
              workDone:
                'With most of the clients, we always tried to have the UAT environments deployed to Azure'
            },
            {
              name: 'ASP.Net MVC',
              workDone:
                'Almost all the applications were developed using MVC from ASP.Net, I feel really proud about this experience, because I was the first developer in the company using it, so being the referent helped me developing leadership and technical skills'
            }
          ]
        },
        {
          startDate: '2016/02/02',
          endDate: '2018/05/17',
          role: 'Software developer',
          company: 'Datasoft Netsolutions',
          description:
            "On this job, I visited many clients on their locations inside Costa Rica, understanding their requirements and giving them the best possible solution based on the team's skills and client's budget and infraestructure.",
          implementedTechnologies: [
            {
              name: 'TFS',
              workDone:
                "Almost all the applications's source code was controlled by TFS"
            },
            {
              name: 'Microsoft Azure',
              workDone:
                'With most of the clients, we always tried to have the UAT environments deployed to Azure'
            },
            {
              name: 'ASP.Net MVC',
              workDone:
                'Almost all the applications were developed using MVC from ASP.Net, I feel really proud about this experience, because I was the first developer in the company using it, so being the referent helped me developing leadership and technical skills'
            }
          ]
        },
        {
          startDate: '2016/02/02',
          endDate: '2018/05/17',
          role: 'Software developer',
          company: 'Datasoft Netsolutions',
          description:
            "On this job, I visited many clients on their locations inside Costa Rica, understanding their requirements and giving them the best possible solution based on the team's skills and client's budget and infraestructure.",
          implementedTechnologies: [
            {
              name: 'TFS',
              workDone:
                "Almost all the applications's source code was controlled by TFS"
            },
            {
              name: 'Microsoft Azure',
              workDone:
                'With most of the clients, we always tried to have the UAT environments deployed to Azure'
            },
            {
              name: 'ASP.Net MVC',
              workDone:
                'Almost all the applications were developed using MVC from ASP.Net, I feel really proud about this experience, because I was the first developer in the company using it, so being the referent helped me developing leadership and technical skills'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style scoped>
h3 {
  margin-bottom: 5px;
}
h4 {
  margin-top: 5px;
  margin-bottom: 10px;
}
p {
  margin: 0 5% 0 5%;
  font-size: 15px;
}
</style>
