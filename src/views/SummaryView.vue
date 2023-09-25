<template>
    <div class="content">
      <div class="heading">
        <h1><b><u>Me In  a Minute</u></b></h1>
      </div>
      <p>

I have developed my communication skills by working in the retail market for one year. I have valuable experience of working as a team member with individuals having different mindsets. I have completed 5 group projects both at the university and in the business sector. I have a good understanding of how the retail sector works. I am hardworking and always try to learn from my mistakes.
I am aiming for a position in I.T field, particularly as a Cyber Security Analyst. As, Cyber security is one of the over-glooming fields of the I.T sector. However, my biggest drawback is that I do not have work experience in this field. But I am consistently trying with LinkedIn and CarrerSet at Deakin to find the internships, that I can use as my work experience in this field.
When I finish my studies at Deakin, my unique combination of technical and social abilities, along with my high professional standards and strong motivation, will make me an outstanding graduate.<br>
If You want to navigate any of the webpage. You can select them from the following : - 
        
     </p>
      <div>
        <button @click="activeComp = 'HomeView'">Home</button> <br>
        <button @click="activeComp = 'IntroductionView'">Introduction</button><br>
        <button @click="activeComp = 'WorkExperienceView'">Work Experience</button><br>
        <button @click="activeComp = 'HobbiesView'">Hobbies</button><br> 
        <button @click="activeComp = 'SkillsView'">Skills</button><br> 
        <button @click="activeComp = 'ProjectsView'">Projects</button><br> 
        <button @click="activeComp = 'ContactView'">Contact</button><br> 
        <component :is="activeComp"></component>

        

      </div>
    </div>
  </template>
  
  <script>
     import HomeView from '../views/HomeView.vue';
     import IntroductionView from '../views/IntroductionView.vue';
     import WorkExperienceView from '../views/WorkExperienceView.vue';
     import HobbiesView from '../views/HobbiesView.vue';
     import SkillsView from '../views/SkillsView.vue';
     import ProjectsView from '../views/ProjectsView.vue';
     import ContactView from '../views/ContactView.vue';
  
  export default {
    data() {
      return {
        activeComp: '', // Initially, no component is active
      };
    },
    components: {
    HomeView,
    IntroductionView,  
    WorkExperienceView,
    HobbiesView,
    SkillsView,
    ProjectsView, 
    ContactView
    },
  };
  </script>
  
  <style>
  .heading {
    color: darkslateblue;
  }
  
  .content{
    background-color: yellowgreen;
    color: darkviolet;
    width:fit-content;
    padding: 10px;
 
  
  }
  </style>
  