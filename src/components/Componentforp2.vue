<template>
    <div class="content_1">
      <div id="intro_1">
        <h1><u><b>My Second Project</b></u></h1>
      </div>
      <p>
        In my final year of high school, I embarked on a project to create a solar-powered phone charger, merging my fascination with renewable energy and technology.
        Armed with solar cells, a charge controller, and a rechargeable battery, I designed a portable charger capable of harnessing sunlight and storing energy for charging smartphones.
        Extensive testing revealed its efficiency, offering a green alternative for powering devices.
        I 3D-printed a sleek casing, making it user-friendly and personalized. This project not only broadened my understanding of sustainable tech but also highlighted the real-world impact of innovation and science in addressing modern challenges.
      </p>
      <img src="/solar.jpeg" alt="solar" class="image">
      <div>
        <h2>Charger Status: {{ chargerStatus }}</h2>
        <h2>Battery Status: {{ batteryStatus }}</h2>
        <button @click="startCharging">Start Charging</button>
        <button @click="stopCharging">Stop Charging</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        chargerStatus: 'Not Charging',
        batteryPercentage: 0,
      };
    },
    methods: {
      startCharging() {
        this.chargerStatus = 'Charging';
        // Add logic to start charging
      },
      stopCharging() {
        this.chargerStatus = 'Not Charging';
        // Add logic to stop charging
      },
    },
    computed: {
      batteryStatus() {
        
          return 'Low';
        }
      },
    };
  
  </script>
  
  <style>
  #intro_1 {
    color: yellow;
  }
  
  .content_1 {
    background-color: darkgreen;
    color: lightgreen;
    padding: 10px;
  }
  
  .image {
    margin-left: 180px;
  }
  </style>
  