<template>
  <header class="banner">
    <div class="header-container">
      <img src="/src/assets/imgs/name-header.png" alt="logo" class="logo" />
      <nav>
        <ul class="centered-list">
          <li><a href="/">Home</a></li>
          <li><a href="/projects">Projects</a></li>
          <li><a href="/resume">Resume</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "BannerContent",
};
</script>

<style scoped>
/* General Styles */
.banner {
  background-color: white;
  position: sticky; /* Keeps banner at the top */
  top: 0;
  width: 100%;
  z-index: 1000; /* Ensures it's above other content */
}

.header-container {
  display: flex;
  flex-direction: column; /* Stack image and nav vertically */
  align-items: center; /* Center content horizontally */
  justify-content: center; /* Center content vertically */
  padding: 1rem; /* Add some space around content */
  font-family: "Karla", sans-serif;
}

.logo {
  height: 80px; /* Default logo height */
  max-width: 100%; /* Prevent overflow */
  margin-bottom: 1rem; /* Space between logo and nav */
}

nav ul {
  list-style: none; /* Remove list styling */
  margin: 0;
  padding: 0;
  display: flex; /* Arrange nav items in a row */
  gap: 2rem; /* Add space between nav items */
  justify-content: center; /* Center nav items horizontally */
}

nav li {
  font-size: 1rem; /* Standard font size */
}

nav a {
  color: black;
  text-decoration: none;
  transition: color 0.3s ease; /* Smooth hover transition */
}

nav a:hover {
  color: #5171ff; /* Highlight link on hover */
}

/* Mobile Styles */
@media (max-width: 768px) {
  .header-container {
    flex-direction: column; /* Stack content vertically */
    padding: 1rem; /* Reduce padding for smaller screens */
  }

  .logo {
    height: 60px; /* Smaller logo size */
    margin-bottom: 0.5rem; /* Add spacing below logo */
  }

  nav ul {
    flex-direction: column; /* Stack nav items vertically */
    gap: 1rem; /* Reduce space between items */
  }

  nav li {
    font-size: 0.9rem; /* Adjust font size */
  }
}

@media (max-width: 450px) {
  .logo {
    height: 50px; /* Further reduce logo size */
  }

  nav li {
    font-size: 0.8rem; /* Smaller font for very small screens */
  }

  .header-container {
    padding: 0.5rem; /* Compact padding */
  }
}
</style>
