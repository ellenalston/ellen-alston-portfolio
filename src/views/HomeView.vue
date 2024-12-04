<script setup>
</script>

<template>
  <main>
    <section class="about full-screen d-lg-flex justify-content-center align-items-center" id="about">
        <div class="container">
            <div class="row">

                <div class="col-lg-7 col-md-12 col-12 d-flex align-items-center">
                    <div class="about-text">
                        <h1 class="animated animated-text">
                            <span class="mr-2">Hello World, I'm </span>
                                <div class="animated-info">
                                    <span class="animated-item"> Ellen Alston </span>
                                    <span class="animated-item"> a Software Developer</span>
                                    <span class="animated-item"> a Music Therapist</span>
                                </div>
                        </h1>

                        <p>From music therapy to software development, I bring creativity, empathy, and a passion for innovation to solve problems and make an impact.</p>

                        <div class="custom-btn-group mt-4">
                          <a href="/public/ellen-alston-resume.pdf" target="_blank" class="btn mr-lg-2 custom-btn"><i class='uil uil-file-alt'></i> Download Resume</a>
                        </div>
                    </div>
                </div>

                <div class="col-lg-5 col-md-12 col-12">
                    <div class="about-image svg">
                        <img src="/src/assets/imgs/girl-at-computer.png" class="img-fluid" alt="svg image">
                    </div>
                </div>

            </div>
        </div>
    </section>

  </main>
</template>

<style>
.about-text h1 {
  font-size: 2rem; /* Adjust based on the font size needed */
  line-height: 1.5;
  word-wrap: break-word; /* Ensure words break instead of overflowing */
  display: block; /* Ensure the text behaves in a block layout */
}

.animated-info {
  display: inline-block; /* Make sure items are inline for proper wrapping */
  white-space: normal;  /* Allow wrapping of each item */
  padding-bottom: 20px; /* Add some space between the text and the next element */
}

.animated-item {
  display: inline-block;
  padding: 0 5px; /* Space between text items */
}

@media (max-width: 768px) {
  .about-text h1 {
    font-size: 1.5rem; /* Adjust font size for smaller screens */
    text-align: center; /* Center align text */
  }

  .animated-info {
    display: block; /* Ensure items stack on top of each other on small screens */
    text-align: center; /* Center align items for mobile view */
  }

  .about-text {
    padding: 0 15px; /* Add some padding to prevent text from touching the edges */
  }
}

</style>
