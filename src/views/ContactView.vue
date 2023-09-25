<template>
    <div id="page_container">
      <h1>Contacts</h1>
      <br>
      <p>
        If you want to reach out, you can use the following media handles or can fill the folllowing form:-
      </p>
      <div class="list">
      <ol >
        <li>Instagram: - xxxxxxx</li>
        <li>Facebook: - xxxxxx</li>
        <li> Deakin mail :- s222502703@deakin.edu.au</li>
        <li>Linkdin profile:- www.linkedin.com/in/anmolpreet-singh-ab7648229</li>
      </ol>
    </div>
      <br>
      <!-- Employer Contact Form -->
      <div class="form">
      <h1 class="head">Contact Form for Employers</h1>
      <form>
        <label for="companyName">Company Name:</label>
        <input type="text" id="companyName" v-model="companyName" required><br><br>
  
        <label for="postAvailable">Post Available:</label>
        <input type="text" id="postAvailable" v-model="postAvailable" required><br><br>
  
        <label for="meetingHours">Meeting Hours:</label>
        <input type="text" id="meetingHours" v-model="meetingHours" required><br><br>
  
        <button type="submit">Submit</button>
      </form>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        companyName: '',
        postAvailable: '',
        meetingHours: ''
      }
    }
};
  
  
  </script>
  
  <style>
  #page_container {
    background-color: brown;
    color: yellow;
    width: 1100px;
  }
  
  form {
    margin-top: 20px;
    background-color: darkgreen;
  }
  
 
  
  button {
    background-color: yellowgreen;
 
  }
  
  button:hover {
    background-color: darkgreen;
  }
  .head{
    background-color: lightcoral;
  }
  .list{
    color:lightcyan;
  }
  </style>
  