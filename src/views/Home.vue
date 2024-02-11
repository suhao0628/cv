<template>
  <div class="page">

    <firstpage :basicInformation="basicInformation" :jobIntention="jobIntention" :educationalBackground="educationalBackground" :skills="skills" :certificates="certificates" :project="project"></firstpage>
    <secondpage :project="project" :evaluation="evaluation"></secondpage>
  </div>
</template>

<script>
import firstpage from '../components/firstpage.vue'
import secondpage from '../components/secondpage.vue'
export default {
  name: 'HomeIndex',
  components: {
    firstpage,
    secondpage
  },
  data () {
    return {
      basicInformation: {
        name: 'suhao',
        email: 'suhaoxb@gmail.com'
      },
      jobIntention: {
        position: 'Fullstack Developer/Backend Developer',
        salary: ''
      },
      educationalBackground: {
        graduationSchool: 'Tomsk State University',
        graduationTime: '2025.06',
        major: 'Software Engineering 3rd Year BS'
      },
      certificates: [],
      skills: [
        'Languages: C#, C++, JavaScript,python.Currently learning Golang',
        'Web Frameworks:',
        '  - Backend: ASP.NET Core Web API (RESTful API), ASP.NET Core MVC',
        '  - Frontend: Vue.js/React.js',
        'Authentication/Authorization: JWT, OAuth',
        'Database: EF Core, SQL Server, MySQL',
        'Testing: xUnit, Postman',
        'Version Control: Git, GitHub',
        'Cloud Platforms: Azure',
        'Tools: Visual Studio, VS Code, Swagger'

      ],
      project: {
        first: {
          title: 'Delivery Web',
          desc: 'This project is a web application built for food-delivery service.Including user module,menu module,dish detail module,cart module,order module,admin module.API built using ASP.NET Core WebAPI.Consume api and create front-end pages in MVC application',
          techTags: ['api', 'jwt', 'middleware', 'redis', 'automapper'],
          duty: [
            'Integrated JWT for secure user authentication and authorization.',
            'Utilized AutoMapper to simplify object mapping between data models and DTOs.',
            'Implemented Exception middleware for custom error handling.',
            'Incorporated Redis for caching to improve response times.'

          ]
        },
        second: {
          title: 'Vue-based e-commerce platform',
          techTags: ['Vue3', 'TypeScript', 'axios', 'pinia', 'less', 'Element Plus'],
          desc: 'This is a comprehensive online shopping platform(front-end), including home page module, category module, product details module, login module, shopping cart module, payment module, personal center module.',
          duty: [
            'Front-end interface developed using the Vue3',
            'Encapsulate multiple components to realize component reuse',
            'Encapsulate axios requests, unified token injection using request interceptors, and unified alerts for interface exceptions using response interceptors.',
            'Jumping between pages through declarative and programmatic navigation.'
          ]
        }
      },
      evaluation: [
        'I have passion for web development and continuously enhanced my programming skills through various channels.  I am eager to tackle new challenges, learn emerging technologies'
      ]
    }
  }
}
</script>
<style lang="less" media="print">
.page {
  background-color: #eee;
}
</style>
