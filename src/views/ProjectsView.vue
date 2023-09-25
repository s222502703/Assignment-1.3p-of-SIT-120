<template>
    <div class="page_container">
      <div class="heading">
        <h1><u><b>Projects</b></u></h1>
      </div>
      <p>
        Welcome to my portfolio of projects! I'm excited to share my journey of exploration and creation with you.
        These projects represent my dedication to learning, problem-solving, and innovation in various domains.
        Each one reflects a unique challenge I've taken on, offering a glimpse into my skills and abilities as a learner.
      </p>
  
      <br>
      <Componentforp1 />
      <br>
      <Componentforp2 />
      <br>
      <Componentforp3 />
  
      <div class="selector">
        <label for="favoriteProject">Choose Your Favorite Project:</label>
        <select id="favoriteProject" v-model="userFavoriteProject">
          <option value="p1">Project 1</option>
          <option value="p2">Project 2</option>
          <option value="p3">Project 3</option>
        </select>
        <button @click="submitFavoriteProject">Submit</button>
      
  
      <p v-if="userFavoriteProject !== ''">
        Thank you for choosing {{ projectName(userFavoriteProject) }} as your favorite!

      </p>
      </div>
    </div>
  </template>
  
  <script>
  import Componentforp1 from '../components/Componentforp1.vue';
  import Componentforp2 from '../components/Componentforp2.vue';
  import Componentforp3 from '../components/Componentforp3.vue';
  
  export default {
    components: {
      Componentforp1,
      Componentforp2,
      Componentforp3
    },
    data() {
      return {
        userFavoriteProject: ''
      };
    },
    methods: {
      projectName(projectId) {
        // Map project IDs to project names
        const projectNames = {
          p1: 'Project 1',
          p2: 'Project 2',
          p3: 'Project 3'
        };
        return projectNames[projectId];
      },
      submitFavoriteProject() {
        // Handle submission of the user's favorite project here
        if (this.userFavoriteProject !== '') {
          // You can perform actions like sending the choice to a server or storing it locally
          console.log(`User's favorite project is: ${this.projectName(this.userFavoriteProject)}`);
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .page_container {
    background-color: lightgray;
    padding: 20px;
    font-family: Arial, sans-serif;
    color: darkslateblue;
    margin-left: 80px;
    width: 900px;
  }
  .heading {
    color: darkred;
  }
  .selector{
    background-color: aquamarine;
    color: darkorange;
    font-size: large;
  }
  </style>
  