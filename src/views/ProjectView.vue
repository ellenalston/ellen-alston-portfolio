<template>
  <div class="projects-wrapper">
    <div class="projects">
      <ProjectCard v-for="(project, index) in projects" :key="project.title" :project="project" :index="index" />
    </div>
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
          title: "A.M.P.L.I.F.Y.",
          description: "Advanced Music PlayList Intelligence for You - Full-stack web application using Java, Spring Boot, PostgreSQL, and Vue.js to help music therapists and enthusiasts create curated playlists by filtering 100+ songs based on detailed metadata, including key, tempo, genres, and themes. Integrated YouTube video embedding and advanced search tools for seamless music discovery and session planning.",
          image: "/imgs/amplify.png",
          skills: ["Java", "Spring Boot", "Spring Data JDBC", "PostgreSQL", "Vue.js", "JavaScript", "HTML", "CSS", "JSON", "RESTful APIs"],
          links: {
            github: "https://github.com/ellenalston/mt-playlist-generator",
            site: null,
          }
        },

        {
          title: "Junior Dev Job Search Portal",
          description: "This application helps organize and manage my job search as a Junior Developer, tracking companies, applications, and positions. It utilizes Spring Boot, Vue.js, and PostgreSQL to provide a full-stack solution while keeping my skills sharp during the job search process.",
          image: "/imgs/junior-dev-search.png",
          skills: ["Java", "Spring Boot", "Spring Data JDBC", "PostgreSQL", "Vue.js", "JavaScript", "HTML", "CSS", "JSON", "RESTful APIs"],
          links: {
            github: "https://github.com/ellenalston/job-search-companies",
            site: null,

          }
        },
        {
          title: "Baking Conversion App",
          description: "The Baking Conversion Tool is a simple web application that allows users to convert between different units of measurement commonly used in baking. Users can input a measurement in one unit and receive the equivalent amount in another unit. The supported units include ounces, milliliters, cups, tablespoons, and teaspoons.",
          image: "/imgs/baking-computer.png",
          skills: ["HTML", "CSS", "JavaScript"],
          links: {
            github: "https://github.com/ellenalston/baking-conversions",
            site: "https://baking-conversions.netlify.app/",
          },
        },

        {
          title: "Pizza Ordering App",
          description: "This is a pair of applications (with a shared backend) for a pizzeria. The first allows customers to order pizzas, either from a list of pre-configured options or create their own. The second enables the pizzeria employees to keep track of customer orders and update the menu of available options.",
          image: "/imgs/pizza-capstone.png",
          skills: ["Java", "Spring Boot", "PostgreSQL", "Vue.js", "JavaScript", "HTML", "CSS", "JSON", "RESTful APIs"],
          links: {
            github: "https://github.com/ellenalston/pizza-ordering-capstone",
            site: null,
          }
        },

        {
          title: "Music Therapy Playlist Generator",
          description: "This database helps music therapists create session-specific playlists by organizing songs, genres, themes, and their relationships. It stores details about songs, genres, and themes, and how they are linked. Plans are in place to expand it into a full-stack application.",
          image: "/imgs/mt-playlist.png",
          skills: ["PostgreSQL", "SQL", "Database Design", "Data Modeling", "pgAdmin"],
          links: {
            github: "https://github.com/ellenalston/music-therapy-playlist",
            site: null,
          }
        },

        {
          title: "Vending Machine Simulator",
          description: " Developed a Vending Machine Application utilizing object-oriented principles, featuring polymorphism for item-specific purchase messages, dynamic file I/O for inventory loading and transaction logging via Scanner and PrintWriter, and enhanced maintainability through inheritance, method overriding, and efficient resource management.",
          image: "/imgs/vending-machine.png",
          skills: ["Java", "Object-Oriented Programming", "File I/O", "Scanner", "PrintWriter"],
          links: {
            github: null,
            site: null,
            askForCode: true,
          }
        },
        {
          title: "Tenmo Mock Money Transfer App",
          description: "Pair-programmed a RESTful API server and command-line Venmo-styled application for simulating peer-to-peer money transfers, featuring secure user authentication and transaction management.",
          image: "/imgs/tenmo.png",
          skills: ["Java", "Spring Boot", "PostgreSQL", "RESTful APIs", "DAO Testing", "CLI"],
          links: {
            github: null,
            site: null,
            askForCode: true,
          }
        }

        // Add more projects as needed
      ],
    };
  },
};
</script>

<style scoped>
/* Add padding to the body to ensure space on the sides */
body {
  margin: 0;
  padding: 0 20px;
  /* Add horizontal padding to the body */
}

/* Wrapper for the projects container to prevent overflow */
.projects-wrapper {
  max-width: 100%;
  box-sizing: border-box;
  padding: 20px;
  /* Add padding to the sides of the container */
  overflow: hidden;
  /* Prevents content from spilling out */
}

/* Projects grid layout */
.projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

/* Alternating Colors for cards */
.project-0 {
  background-color: #aadec5;
}

.project-1 {
  background-color: #e5f0fc;
}

.project-2 {
  background-color: #ff8288;
}

.project-3 {
  background-color: #f9f5e7;
}

@media (max-width: 768px) {
  .projects {
    grid-template-columns: 1fr;
    /* Single column on smaller screens */
  }
}
</style>
