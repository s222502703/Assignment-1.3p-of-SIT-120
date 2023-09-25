<template>
    <div id="page_container">

        <div id="heading"><h1><b>Welcome to My Portfolio</b></h1>

</div>
  
    
  
      Hello, I'm Anmolpreet Singh, and I'm excited to welcome you to my online portfolio. This is where I showcase my passion for creativity, problem-solving, and innovation through a collection of projects that reflect my journey as a Your Profession.
  
      Throughout my career, I've had the privilege of working on a diverse range of projects, each one presenting unique challenges and opportunities. From designing intuitive user interfaces to developing robust software solutions, I've had the chance to collaborate with amazing teams and clients to bring ideas to life.
  
      This portfolio is not just a showcase of my work; it's a testament to my commitment to excellence. I believe in the power of technology and design to transform the way we live and work, and I'm dedicated to making a positive impact through my skills and expertise.
  
<br>
<br>
      Feel free to explore my projects, read about my experiences, and get to know me better. Whether you're a fellow professional, a potential client, or just someone curious about what I do, I hope you find inspiration in these pages.
  
      Thank you for visiting, and please don't hesitate to reach out if you'd like to collaborate or simply have a conversation. Let's connect and explore the possibilities together.
    <br>
      Sincerely,
    <br>
      Anmolpreet Singh
      
      <div id="ratings">
      <div id="star-container">

        <span class="star" @click="rate(1)">★</span>
        <span class="star" @click="rate(2)">★</span>
        <span class="star" @click="rate(3)">★</span>
        <span class="star" @click="rate(4)">★</span>
        <span class="star" @click="rate(5)">★</span>
      </div>
    </div>
    <footer>
      <div id="footer-content">
        <p>Discalimer:- It has my personal Information. So, It should be not forwarded to anyone else without notifying me. Otherwise, Legal Action will be taken ...</p>
      </div>
    </footer>
    </div>
  </template>
  <script>
export default {
  methods: {
    rate(rating) {
      
      alert(`You rated this introduction as ${rating} stars.`);
    }
  }
};

</script>
  <style scoped>
   #page_container {
    background-color: darkcyan;
    margin: auto;
    width: 1100px;
    color: lightyellow;
    margin-left:50px;
    padding: 10px;
    
  }
  #heading{
    color:lime;
    text-align: center;
  }
  #star-container {
    font-size: 24px;
    cursor: pointer;
  }
  
  #ratings {
    margin: 20px;
    text-align: right;
  }
  footer {
  background-color: darkgray;
  color: lightyellow;
  text-align: center;
  padding: 10px;
}

  </style>
  