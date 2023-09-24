<template>
  <div class="page-container">
    <nav class="nav-stack">
      <link rel="icon" type="image/x-icon" href="/web/favicon.ico">

      <div class="logo">
      <img src="/profile.jpg" alt="myphoto" class="logo-image" />
    </div>
      <div class="nav-links">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/Introduction">Introduction</RouterLink>
        <RouterLink to="/WorkExperience">Work Experience</RouterLink>
        <RouterLink to="/Hobbies">Hobbies</RouterLink>
        <RouterLink to="/Skills">Skills</RouterLink>
        <RouterLink to="/Projects">Projects</RouterLink>
        <RouterLink to="/Contact">Contact</RouterLink>
        <RouterLink to="/Summary">Summary</RouterLink>
       
      </div>
    </nav>
    <RouterView />
  </div>
</template>

<style scoped>
/* Styling for the page container */
.page-container {
  display: flex;
  flex-direction: row; /* Horizontal layout */
  align-items: flex-start; /* Align items to the top */
}

/* Styling for the navigation menu */
nav.nav-stack {
  min-width: 150px; /* Set a minimum width for the navigation menu */
  max-width: 40%; /* Set a maximum width for the navigation menu */
  background-color: grey;
  color: whitesmoke;
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  padding: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

nav.nav-stack img {
  margin-bottom: 1rem;
}

.nav-links {
  display: flex;
  flex-direction: column;
  font-size: larger;
  height: auto;
 
}

nav.nav-stack a {
  text-decoration: none;
  color: var(--color-text);
  padding: 1rem;
  transition: background-color 0.3s, color 0.3s;
}

nav.nav-stack a:hover {
  background-color: black;
  color: red;
}

/* Styling for the main content */
header {
  line-height: 1.5;
  max-height: 100vh;
  flex-direction: column;
  align-items: center; /* Center horizontally */
  justify-content: center; /* Center vertically */
  height: 100vh; /* Use the full viewport height */
}
.logo {
  text-align: center; /* Center the image horizontally */
}

/* Add the following CSS to adjust the image size */
.logo-image {
  max-width: 200px; /* Adjust the maximum width as needed */
  max-height: 200px; /* Adjust the maximum height as needed */
}


/* Media query for larger screens */
@media (min-width: 1024px) {
  /* Adjust the margin-left to make space for the fixed navigation menu */
  .page-container {
    margin-left: 150px; /* Adjust the margin to match the width of the navigation menu */
  }
}
</style>