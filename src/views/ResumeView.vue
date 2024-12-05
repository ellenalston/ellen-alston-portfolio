<template>
  <div class="resume-container">
    <div class="pdf-viewer">
      <PdfApp style="height: 90vh; width: 100%;" pdf="/ellen-alston-resume.pdf" />
    </div>
  </div>
</template>

<script>
import PdfApp from "vue3-pdf-app";
import "vue3-pdf-app/dist/icons/main.css";

export default {
  name: "ResumeView",
  components: {
    PdfApp,
  },
};
</script>

<style scoped>
/* Center and limit the width of the container */
.resume-container {
  min-width: 90%; /* Adjust this value for your desired width */
  max-width: 1000px; /* Limit the maximum width */
  margin: 0 auto; /* Centers the container horizontally */
  padding: 20px; /* Optional: Add some padding around the content */
  text-align: center; /* Center the content */
  display: flex;
  flex-direction: column;
  justify-content: space-between; /* Ensure space is distributed */
  height: 100vh; /* Take up full height of the screen */
}

/* Ensure the PDF viewer respects the container width */
.pdf-viewer {
  border: 1px solid #ccc; /* Optional: Add a border to make it visually distinct */
  border-radius: 8px; /* Optional: Round the corners */
  position: relative; /* Ensure the container is positioned relative to the parent */
  z-index: 1; /* Ensure the viewer is above other content */
  margin-top: 15px; /* Optional: Add some space between the content */
  flex-grow: 1; /* Allow the viewer to take available space */
  margin-bottom: 20px; /* Add space between the viewer and the bottom */
}

.pdf-app {
  height: 100%;
  width: 100%;
}
</style>
