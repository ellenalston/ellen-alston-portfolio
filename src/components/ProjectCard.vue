<template>
  <div :class="['project', `project-${index % 4}`]">
    <img :src="project.image" :alt="project.title" />
    <div>
      <h2>{{ project.title }}</h2>
      <div class="links">
        <a v-if="project.links.github" :href="project.links.github" target="_blank">GitHub</a>
        <a v-if="project.links.site" :href="project.links.site" target="_blank">Live Site</a>
        <span v-if="project.links.askForCode">Ask for Code</span>
      </div>
      <p>{{ project.description }}</p>
      <ul class="skills">
        <li v-for="skill in project.skills" :key="skill">{{ skill }}</li>
      </ul>

    </div>
  </div>
</template>


<script>
export default {
  props: {
    project: Object,
    index: Number, // Pass the index of the project from the parent component
  },
};
</script>

<style scoped>
/* Base container styling */
.project {
  display: flex;
  flex-direction: column;
  /* Stack items vertically */
  align-items: center;
  /* Align items to the left */
  text-align: center;
  gap: 20px;
  /* Space between image, text, and links */
  margin: 20px 0;
  background-color: #f9f5e7;
  /* Light background color for the project card */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  /* Subtle shadow for depth */
}

/* Image styling */
.project img {
  align-self: center;
  /* Center the image */
  width: 100%;
  /* Image takes full width */
  max-width: 300px;
  /* Restrict maximum size */
  height: auto;
  /* Maintain aspect ratio */
  border-radius: 8px;
  /* Optional: Rounded corners */
}

/* Text container */
.project div {
  flex: 1;
  /* Allow the text container to grow and take up space */
  width: 100%;
  /* Full width */
}

/* Title */
.project h2 {
  font-size: 1.5rem;
  color: #000076;
  /* Blue title */
  margin-bottom: 10px;
}

/* Description */
.project p {
  font-size: 1rem;
  line-height: 1.5;
  color: #465aa5;
  /* Blue text */
  margin-bottom: 10px;
}

/* Skills list */
.skills {
  display: flex;
  /* Lay out skills inline */
  flex-wrap: wrap;
  /* Allow skills to wrap to new rows */
  justify-content: center;
  /* Center-align skills */
  gap: 10px;
  /* Add spacing between skills */
  list-style-type: none;
  /* Remove bullet points */
  padding: 0;
  margin: 10px 0;
}

.skills li {
  background: #fdac9b;
  /* Pink background for skills */
  padding: 4px 8px;
  border-radius: 4px;
  color: #f9f5e7;
  /* Light text color */
  font-weight: bold;
  font-size: 0.9rem;
}

/* Links container */
.links {
  display: flex;
  /* Arrange links in a row */
  flex-wrap: wrap;
  /* Allow wrapping of links/buttons */
  justify-content: center;
  /* Center-align links */
  gap: 10px;
  /* Add spacing between links */
  margin-top: auto;
  /* Push links to the bottom of the card */
}

.links a,
.links span {
  color: #e5f0fc;
  /* Yellow text for links */
  text-decoration: none;
  font-weight: bold;
  padding: 6px 10px;
  border-radius: 4px;
  font-size: 0.9rem;
  background: #000076;
  /* Add background color for buttons */
  color: #f9f5e7;
  /* Light text color */
}

.links a:hover {
  text-decoration: underline;
  background: #fdac9b;
  /* Pink hover background */
  color: #f9f5e7;
  /* Light hover text color */
}

/* Additional styling for Ask for Code */
.links span {
  background: #000076;
  /* Pink background for Ask for Code */
  color: #f9f5e7;
  /* Light text color */
  font-size: 0.9rem;
  padding: 6px 10px;
  display: inline-block;
  border-radius: 4px;
}

/* Responsive design */
@media (max-width: 768px) {
  .project {
    flex-direction: column;
    /* Stack content vertically */
    align-items: center;
    /* Center-align content for a clean look */
  }

  .project img {
    width: 100%;
    /* Image takes full width on smaller screens */
    max-width: none;
  }

  .skills {
    justify-content: center;
    /* Center-align skills for better appearance */
  }

  .links {
    justify-content: center;
    /* Center-align buttons */
  }
}

@media (max-width: 425px) {
  .project h2 {
    font-size: 1.2rem;
    /* Smaller title for small screens */
  }

  .project p {
    font-size: 0.9rem;
    /* Adjust description size */
  }

  .skills li {
    font-size: 0.8rem;
    /* Smaller skill labels */
    padding: 3px 6px;
    /* Adjust padding for smaller screens */
  }

  .links a,
  .links span {
    font-size: 0.8rem;
    /* Smaller buttons for compact layout */
    padding: 5px 8px;
  }
}
</style>
