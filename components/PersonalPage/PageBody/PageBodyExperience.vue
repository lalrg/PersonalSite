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
              <text-with-elipsis class="text">
                <b>{{ technology.name }}</b>
                : {{ technology.workDone }}
              </text-with-elipsis>
            </li>
          </ul>
        </el-card>
      </el-timeline-item>
    </el-timeline>
  </div>
</template>

<script>
import TextWithElipsis from '~/components/Common/TextWithElipsis'
export default {
  components: { TextWithElipsis },
  data() {
    // I hope data will be migrated to a persistance solution soon :)
    return {
      experiences: [
        {
          startDate: '2018/07/01',
          endDate: '2019/06/28',
          role: 'Advanced Software Engineer',
          company: 'Growth Acceleration Partners (GAP)',
          description:
            'Working with North American clients in large scale applications. I work as a full stack developer, so I always have something to learn :).',
          implementedTechnologies: [
            {
              name: 'Vue JS',
              workDone:
                'Developing new features and maintaining existing ones, working with Element UI'
            },
            {
              name: '.Net Framework',
              workDone:
                'Developing some endpoints to consume from frontend applications and maintaining legacy applications'
            },
            {
              name: '.Net Core',
              workDone:
                'Developing some endpoints to consume from frontend applications.'
            },
            {
              name: 'SQL Server',
              workDone: 'Maintain some stored procedures.'
            },
            {
              name: 'Jenkins',
              workDone:
                'Configuring required new jobs linked to development branches.'
            },
            {
              name: 'Powershell Scripting',
              workDone:
                'Basically maintaining some existing scripts and adapting them to new projects.'
            }
          ]
        },
        {
          startDate: '2018/07/01',
          endDate: '2019/06/28',
          role: 'Software developer',
          company: 'EY (Ernst&Young)',
          description:
            'Internal Development: Solutions for different departments of the company. I learned a lot about how a big company is suposed to work, being involved in some of their big processes and automating some of them integrating a team of multidisciplinary professionals based in Central America.',
          implementedTechnologies: [
            {
              name: 'React JS',
              workDone:
                'Creating a new application, none of the developers were experts in the used technologies, so we had to learn react almost from scratch for that project.'
            },
            {
              name: 'Vue JS',
              workDone:
                'Developing new features and maintaining existing ones for an internal application, written in Vue Js + Typescript + Vuetify. It was not developed following best practices, so I had to refactor some code, develop new features, and fix some bugs almost at the same time.'
            },
            {
              name: '.Net Framework',
              workDone:
                'Supporting some legacy apps, and participating in Architectural Design of new applications.'
            },
            {
              name: '.Net Core',
              workDone:
                'Developing REST APIs that were deployed to Microsoft Azure, connected to SQL Sever databses.'
            },
            {
              name: 'SQL Server',
              workDone:
                'Creating new and maintaining existing stored procedures, and querying data for generating some reports required by different teams. I had to deal with different databases, located in different SQL Server instances and servers, also with different compatibility levels, upgrading databases, and fixing some data loss issues.'
            },
            {
              name: 'SSRS',
              workDone:
                'Generating some automated reports for different departments, creating big stored procedures that involved joining data from multiple sources and comparing/filtering them in different views.'
            },
            {
              name: 'SSIS',
              workDone:
                'There are global and regional environments so we had to make sure the data was updated, in some cases we did not have direct communication between Azure apps and Intranet apps, so we had to develop some SOAP services to consume them in Script Components of SSIS.'
            }
          ]
        },
        {
          startDate: '2017/04/02',
          endDate: '2018/06/01',
          role: 'Web Developer',
          company: 'Datasoft Netsolutions',
          description:
            "On this job, I visited many clients on their locations inside Costa Rica, understanding their requirements and giving them the best possible solution based on the team's skills and client's budget and infraestructure, and also developing solutions with varied technologies.",
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
              name: 'ASP.Net MVC 5',
              workDone:
                'Almost all the applications were developed using MVC from ASP.Net, I feel really proud about this experience, because I was the first developer in the company using it, so being the referent helped me developing leadership and technical skills.'
            },
            {
              name: 'Some Microsoft Certifications',
              workDone: 'You can look at them in my LinkedIn page.'
            }
          ]
        },
        {
          startDate: '2015/02/02',
          endDate: '2017/04/01',
          role: 'Technical Support lead',
          company: 'Datasoft Netsolutions',
          description: 'Technical support for government institution.',
          implementedTechnologies: [
            {
              name: 'Team leadership',
              workDone: 'Coordinating a team of 4 technical support analysts.'
            },
            {
              name: 'Reporting',
              workDone: 'Varied reports of tickets resolution and inventories.'
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
