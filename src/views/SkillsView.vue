<template>
  <div class="skills-container">
    <h1><u>My Skills and Qualities</u></h1>

    <form @submit.prevent="addSkill">
      <label for="skillName">Skill/Quality:</label>
      <div class="entry">
        <input type="text" id="skillName" v-model="newSkill" required />
      </div>
      <button type="submit">Add Skill/Quality</button>
    </form>

    <div class="skills-list">
      <h2>My Skills and Qualities List:</h2>
      <ul> <!-- Wrap your <li> elements in an <ol> element for an ordered list -->
        <li v-for="(skill, index) in skills" :key="index">
          {{ skill }}
          <button @click="removeSkill(index)">Remove</button>
        </li>
      </ul>
    </div>
  </div>
</template>

  
  <script>
  // Import the external CSS file using the correct format
  import './SkillStyling.css';
  
  export default {
    data() {
      return {
        newSkill: '', // Stores the new skill/quality
        skills: []     // Array to store skills/qualities
      };
    },
    methods: {
      addSkill() {
        if (this.newSkill.trim() !== '') {
          this.skills.push(this.newSkill);
          this.newSkill = ''; // Clear the input field after adding
        }
      },
      removeSkill(index) {
        this.skills.splice(index, 1);
      }
    }
  };
  </script>
  