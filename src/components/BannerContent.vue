<template>
  <header>
    <div class="header-container">
      <img src="/src/assets/imgs/name-header.png" alt="logo" />
      <nav>
        <ul class="centered-list">
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
          <li><a href="/projects">Projects</a></li>
          <li><a href="/contact">Resume</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data() {
  }
};
</script>

<style scoped>
img {
  height: 100px;
}
body {
  margin: 0;
  padding: 0;
  height: 100%;
  background-color: white;
}

.header-container {
  height: 15vh;
  display: flex;
  flex-direction: column;
  justify-content: center; /* Centers nav horizontally in the header */
  align-items: center; /* Centers nav vertically */
  font-family: "Karla", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

nav ul {
  list-style: none; /* Remove default list styles */
  margin: 0;
  padding: 0;
  display: flex; /* Display nav items in a row */
  justify-content: center; /* Centers list items horizontally */
  gap: 2rem; /* Adds spacing between items */
}

nav li {
  font-size: 1rem;
}

nav a {
  color: black;
  text-decoration: none;
}

header {
  background-color: white;
  position: sticky; /* Makes the header stay at the top when scrolling */
  top: 0;
  width: 100%;
  z-index: 1000; /* Ensure it stays on top */
  /* box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1); */
  height: 15vh;
}


</style>
