<template>
  <div class="main">
      <h1>Portfolio</h1>
      <p>Welcome to my portfolio site! Here are some of the things I've been working on.</p>
      <div class="project-list">
          <project-render :project="projectList.personalWeatherApp"></project-render>
          <project-render :project="projectList.comicbookCollection"></project-render>
          <project-render :project="projectList.portfolioSite"></project-render>
      </div>
  </div>
</template>

<script>
import ProjectRender from './ProjectRender.vue';
export default {
    components: {
        ProjectRender
    },
    data() {
        return {
            loading: true,
            projectList: 
            {
                 personalWeatherApp: 
                {
                    title: 'Personal Weather App',
                    description: 'Mostly just for fun, this is my first deployment to Heroku. This app displays information about the weather conditions outside my house. The information is pulled from the OpenWeatherMap API and is avaliable in different temperature units. The image and the image\'s color dynamically update depending on the current conditions.',
                    img: 'weather.png',
                    demoLink: 'https://outside-weather.herokuapp.com/',
                    sourceCode: 'https://github.com/wade-loccisano/outside-weather',
                    technologies:
                    [
                        'HTML',
                        'CSS',
                        'JavaScript',
                        'Vue.js',
                        'Axios',
                        'Bootstrap',
                        'OpenWeatherMap API',
                        'Git',
                        'Node.js'
                    ]
                },
                comicbookCollection: 
                {
                    title: 'Comic Book Collection',
                    description: 'My group\'s final project for Tech Elevator\'s Java Development bootcamp, ' +
                     'this project is a web app built with ' + 
                     'Vue.js and Spring Boot. Users can log in and ' + 
                     'create comic book collections with information dynamically pulled with Marvel\'s ' +
                     'API. All user information is stored in our custom SQL database.',
                    img: 'comicbook.png',
                    demoLink: '',
                    sourceCode: 'https://github.com/wade-loccisano/comicbook-collection',
                    technologies:
                    [
                        'HTML',
                        'CSS',
                        'JavaScript',
                        'Vue.js',
                        'Axios',
                        'Marvel API',
                        'Java',
                        'SpringBoot',
                        'PostgreSQL'
                    ]
                },
                portfolioSite: 
                {
                    title: 'Portfolio Site',
                    description: 'Source code for this portfolio site. My design goals were simplicity and minimalism while allowing for easy additions using Vue components. Site is now responsive for mobile viewing.',
                    img: 'portfolio.png',
                    demoLink: '',
                    sourceCode: 'https://github.com/wade-loccisano/web-portfolio',
                    technologies:
                    [
                        'HTML',
                        'CSS',
                        'JavaScript',
                        'Vue.js',
                        'Bootstrap',
                        'Git',
                    ]
                },
            }
        }
    }
}
</script>

<style scoped>

</style>