<template>
    <div class="page_container">
      <h1><u>My Hobbies</u></h1>
      <br>
      <div class="hobbies-grid">
        <div class="hobby-item" v-for="(hobby, index) in hobbies" :key="index">
          <h2>{{ hobby.name }}</h2>
          <img :src="hobby.image" :alt="hobby.name" class="hobby-image" />
          <p>{{ hobby.description }}</p>
        </div>
        <br>
      </div>
      <div class="matcher">
      <p>How many my Hobbies matched with your's : - </p>
      <div class="function">
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>                   
      <p>Count: {{ count }}</p>
    </div>
    </div>
    </div>
  </template>
  
  <script >
  import { ref } from 'vue'; 
  export default {
    data() {
      return {
        hobbies: [
          {
            name: 'Music',
            image: '/Music.jpeg',
            description: 'I love hearing the Music. I am fond of both western music and Punjabi Music.Moreover, I also create some soothing beats in my free time. ',
          },
          {
            name: 'Gardening ',
            image: '/gardening.jpeg',
            description: 'Gardening is my therapy. Getting my hands dirty in the soil, nurturing plants, and watching them flourish is not just my hobby, but a way to connect with nature and find tranquility.',
          },
          {
            name: 'Reading',
            image: '/reading.jpeg',
            description: 'Reading is my lifelong companion. Whether its getting lost in the pages of a novel, learning from non-fiction, or exploring different cultures through literature, books open up new horizons for me.',
          },
          {
            name:'Volleyball',
            image:'/Volleyball.jpeg',
            description:'Volleyball is my absolute favorite hobby. There is something incredibly satisfying about the sensation of my hands connecting with the ball, sending it soaring over the net. The teamwork and camaraderie on the court make it even more enjoyable.'
          },
          {
            name:'Yoga',
            image:'/Yoga.jpeg',
            description:'Yoga is my daily ritual for mind and body balance. It helps me find inner peace, flexibility, and strength. Through yoga, I connect with my breath and cultivate mindfulness in a fast-paced world.'
          }
        ],
      };
    },
    setup() {
    const count = ref(0);

    const increment = () => {
      count.value++;
    };

    const decrement = () => {
      count.value--;
    };

    return { count, increment, decrement };
  },
  };
  </script>
  
  <style scoped>
  .page_container {
    background-color: darkgreen;
    color: yellow;
    padding: 15px;
    text-align: center;
    width:1100px;
  }
  
  h1 {
    color: lightcyan;
  }
  
  .hobbies-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 20px;
    justify-content: center;
    align-items: start;
  }
  
  .hobby-item {
    background-color: skyblue;
    padding: 15px;
    text-align: center;
    border-radius: 10px;
  }
  
  .hobby-image {
    max-width: 100%;
    height: auto;
    border-radius: 10px;
    margin: 10px 0;
  }
  
  p {
    color: darkviolet;
  }
  .matcher{
    background-color: lightgreen;
  }
  </style>