<template>
  <div class="page_container">
    <div class="heading">
      <h1><b>Introduction</b></h1>
    </div>

    <p>It's Anmolpreet Singh on this side. My home country is India, and I am currently in Australia as an International Student. I am currently enrolled in Bachelor of Information Technology at Deakin University. I am in my first year at the moment and currently looking for job opportunities in the IT field.</p>
    <div class="heading_1">
    <h2>My Study Background</h2>
  </div>
    <br>
    <table class="study-table">
      <thead>
        <tr>
          <th>Study Level</th>
          <th>Marks</th>
          <th>Completed In</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Class 10</td>
          <td>94%</td>
          <td>2019</td>
        </tr>
        <tr>
          <td>Class 12</td>
          <td>85.6%</td>
          <td>2021</td>
        </tr>
        <tr>
          <td>Bachelor Degree</td>
          <td>....</td>
          <td> In 2025</td>
        </tr>
       
      </tbody>
    </table>
    <br>
    <div class="plus_point">
    Plus Point: - I have given the Joint Entrance Exam , which is India 2nd hardest exam to crack. I gave that exam in 2002 and got 
    80 percentile in that and received overall 1,80,0000 th rank in overall India and got government seat in Bachelor  of Computer 
    Science at Guru Nanak Dev University.Guru Nanak Dev University is accredited A++ grade at World level Universities. 
     I have completed two semesters there and I passed both semesters in first divsion. Thereafter, I moved to Australia for my further
     higher Education...

  </div>
  <div id="info">
   If You want to know about JEE exam <a href="https://www.nta.ac.in/Engineeringexam">@click here. </a><br>
   If you want to know about G.N.D.U <a href="https://online.gndu.ac.in">@click here.</a>
  </div>
    <br>
    <div id="checker">
  <p>Select your Satisfaction rate(For  employers): - </p>
  <button @click="selectExcellent">Excellent</button><br>
  <button @click="selectDecent">Decent</button>
  <br>
  <div v-if="selectedOption === 'Excellent'">
  <p>Congratulations! The employer is satisfied with the qualifications.</p>

</div>

<div v-else-if="selectedOption === 'Decent'">
  <p>Ohh! You still need to work more to meet the employer's expectations.</p>
    </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
      return {
        selectedOption: '' ,
        
      }
    },
    methods: {
      selectExcellent() {
        this.selectedOption = 'Excellent';
      },
      selectDecent() {
        this.selectedOption = 'Decent';
      }
    }
};
</script>
<style scoped>
.page_container {
  background-color: darkviolet;
  color: burlywood;
  margin-left: 50px;
  padding: 10px;
  width: 900px;
}

.heading {
  color: darkorange;
  font-size: xx-large;
}
.heading_1{
  color:lightseagreen;
  font-size: large;
}
/* Style for the table */
.study-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
}

.study-table th,
.study-table td {
  border: 1px solid burlywood;
  padding: 8px;
  text-align: center;
}

.study-table th {
  background-color: darkorange;
  color: white;
}
#checker{
        display: inline-block;
      padding: 10px;
      font-size: x-large;
      background-color: lightskyblue;
      color: darkblue
    }

.plus_point{
  background-color: darkred;
  color: lightyellow;
  font-size: large;
}

</style>
