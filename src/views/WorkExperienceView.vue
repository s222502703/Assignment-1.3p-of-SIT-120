<template>
  <div class="page_container">
    <div id="heading">
      <h1><b><u>Work Experience</u></b></h1>
    </div>
    <p>
      Unfortunately, I don't have experience in the I.T field yet. But, I have worked in other sectors, which has helped me learn new skills from others. The main skills that I have learned are :-
    </p>
    <ul>
      <li>Communication: Now, I can communicate with anyone regardless of their age, gender, and race.</li>
      <li>Time Management: I have improved my time management skills.</li>
      <li>Discipline: I can do those things with my focus that I don't want to.</li>
      <li>Confidence: I have developed the feelings to go beyond my limit.</li>
    </ul>
    <br />
    <div class="experience">
      <h2>My Work Experiences:</h2>
      <div class="experience-grid">
        <div v-for="(experience, index) in workExperiences" :key="index" class="experience-item">
          <div class="company-info">
            <img :src="experience.companyImage" alt="Company Logo" class="company-logo" />
            <strong>{{ experience.companyName }}</strong>
          </div>
          <ul>
            <li>Years of Experience: <input v-model="experience.yearsOfExperience" /></li>
            <li>Location: <input v-model="experience.location" /></li>
            <li>Post: <input v-model="experience.post" /></li>
            <li>Duties:</li>
            <ul>
              <li v-for="(duty, dIndex) in experience.duties" :key="dIndex">
                <input v-model="experience.duties[dIndex]" />
              </li>
              <li>
                <button @click="addDuty(experience)">Add Duty</button>
              </li>
            </ul>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      workExperiences: [
        {
          companyName: "United Petroleum Station",
          companyImage: "/fuel.png",
          yearsOfExperience: "",
          location: "",
          post: "",
          duties: [""]
        },
        {
          companyName: "Woolworths",
          companyImage: "/woolies.jpg",
          yearsOfExperience: "",
          location: "",
          post: "",
          duties: [""]
        },
        {
          companyName: "Khalsa-Aid Foundation",
          companyImage: "/khalsa.jpeg",
          yearsOfExperience: "",
          location: "",
          post: "",
          duties: [""]
        }
      ]
    };
  },
  methods: {
    addDuty(experience) {
      experience.duties.push("");
    }
  }
};
</script>

<style scoped>
.page_container {
  background-color: lightsalmon;
  width: 900px;
  max-width: 100%; /* Ensure it doesn't exceed the viewport width */
  margin: 0 auto; /* Center the container horizontally */
  padding: 5px;
  color: blue;
}

#heading {
  color: darkred;
}

.experience {
  background-color: darkviolet;
  color: darkblue;
  max-width: 100%;
}

.experience-grid {
  display: grid;
  grid-template-columns: repeat(1); /* One column */
  gap: 5px;
  max-width: 100%;
}

.experience-item {
  display: flex;
  background-color: white;
  padding: 20px;

}

.company-info {
  flex: 1;
  display: flex;
  margin-left:50px;
  text-align: center;

}

.company-logo {
  max-width:150px;
  margin-right: 20px;
}
</style>
