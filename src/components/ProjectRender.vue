<template>
  <div class="individual-card">
    <div class="col d-flex justify-content-center mt-4">
      <b-card
        img-left
        style="max-width: 55rem;"
        class="mb-3"
      >
      <b-row no-gutters>
          <b-col md="6">
              <b-card-img :src="`img/${project.img}`" alt="Image of the project" class="border border-secondary"></b-card-img>
          </b-col>
          <b-col md="6">
      <b-card-body class="card-info">
          <b-card-title>{{ project.title }}</b-card-title>
          <b-card-sub-title class="mb-2">
                <ul class="technologies-list">
                    <li class="technology" v-for="(tech, index) in project.technologies" :key="index">
                        {{ tech }}
                    </li>
                </ul>
          </b-card-sub-title>
        <b-card-text>{{ project.description }}</b-card-text>
        <div class="demo-links">
          <b-row v-if="project.demoLink.length != 0">
            <b-col md="6" class="mt-2">
              <a :href="`${project.demoLink}`"><button class="btn btn-secondary">Demo</button></a>     
            </b-col>
            <b-col md="6" class="mt-2">
              <a :href="`${project.sourceCode}`"><button class="btn btn-secondary">Github</button></a>     
            </b-col>
          </b-row>
          <div v-if="project.demoLink.length == 0">
            <a :href="`${project.sourceCode}`"><button class="btn btn-secondary mt-2">Github</button></a>  
          </div>
        </div>
      </b-card-body>
          </b-col>
      </b-row>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
    props: ["project"]
};
</script>

<style>
.card-body {
  background-color: #F5F5F5;
}
.card-info {
  padding-top: 0 !important;
}
.card-img {
    width: 100%;
    height: 22vw;
    object-fit: cover;
}
.technologies-list {
    list-style: none;
    padding-inline-start: 0;
}
.technology {
  display: inline-block;
  margin: 0.2rem;
  border: 1px solid red;
  padding: 5px;
  border-radius: 5px;
}
</style>