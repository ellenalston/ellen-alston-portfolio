<template>
  <div class="projects">
    <ProjectCard v-for="(project, index) in projects"
      :key="project.title"
      :project="project"
      :index="index"/>
  </div>
</template>

<script>
import ProjectCard from "../components/ProjectCard.vue";

export default {
  components: { ProjectCard },
  data() {
    return {
      projects: [
      {
          title: "Baking Conversion App",
          description: "The Baking Conversion Tool is a simple web application that allows users to convert between different units of measurement commonly used in baking. Users can input a measurement in one unit and receive the equivalent amount in another unit. The supported units include ounces, milliliters, cups, tablespoons, and teaspoons.",
          image: "/src/assets/imgs/baking-computer.png",
          skills: ["HTML", "CSS", "JavaScript"],
          links: {
            github: "https://github.com/ellenalston/baking-conversions",
            site: "https://baking-conversions.netlify.app/",
          },
        },

        {
          title: "Pizza Ordering App",
          description: "This is a pair of applications (with a shared backend) for a pizzeria. The first allows customers to order pizzas, either from a list of pre-configured options or create their own. The second enables the pizzeria employees to keep track of customer orders and update the menu of available options.",
          image: "/src/assets/imgs/pizza-capstone.png",
          skills: ["Java", "Spring Boot", "PostgreSQL", "Vue.js", "JavaScript", "HTML", "CSS", "JSON", "RESTful APIs"],
          links: {
            github: "https://github.com/ellenalston/pizza-ordering-capstone",
            site: null,
        }
      }
        // Add more projects as needed
      ],
    };
  },
};
</script>

<style scoped>
.projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}
/* Alternating Colors for cards */

.project-0 {
  background-color: #f9f5e7; /* Light beige */
}

.project-1 {
  background-color: #e5f0fc; /* Dark blue */
}

.project-2 {
  background-color: #7accb2; /* Teal */
}

.project-3 {
  background-color: #ff8288; /* Coral */
}

.project-4 {
  background-color: #f0f4c3; /* Light green */
}

@media (max-width: 768px) {
  .projects {
    grid-template-columns: 1fr; /* Single column on smaller screens */
  }
}
</style>

