<template>
  <q-page class="no-padding">
    <!-- Hero Parallax Section -->
    <q-parallax 
      :src="backgroundImage" 
      :height="800"
      :speed="0.5"
      class="text-white custom-parallax"
    >
      <!-- Dark overlay for better text readability -->
      <div class="parallax-overlay"></div>
      
      <!-- Hero content -->
      <div class="absolute-full flex flex-center">
        <div class="text-center q-pa-xl" style="z-index: 2;">
          <h1 class="text-weight-bold q-mb-md font-poppins">
            HI!
          </h1>
          <p class="text-h6 text-md-h5 q-mb-xl font-inter">
            My name is Cong.<br/> Nice to E-meet you!
          </p>
          <q-btn 
            text-color="white" 
            size="lg" 
            label="View My Resume" 
            class="q-px-xl"
            outline
            :href="resumePdf"
            target="_blank"
            icon="description"
          />
        </div>
      </div>
    </q-parallax>

    <!-- Additional content sections for scrolling -->
    <div class="about-section text-white q-pa-xl" :style="aboutSectionStyle">
      <!-- Dark overlay for better text readability -->
      <div class="about-overlay"></div>
      <div class="row justify-center" style="position: relative; z-index: 2;">
        <div class="col-12 col-md-8 text-center">
          <h2 class="text-h3 q-mb-lg font-poppins">About Me</h2>
          <p class="text-h6 font-inter q-mb-xl">
            Passionate weightlifter and problem solving through programming.
          </p>
        </div>
      </div>
    </div>

    <!-- Skills section with background -->
    <div class="skills-section text-white q-pa-xl" :style="skillsSectionStyle">
      <!-- Dark overlay for better text readability -->
      <div class="skills-overlay"></div>
      <div class="row justify-center" style="position: relative; z-index: 2;">
        <div class="col-12 col-md-8 text-center">
          <h2 class="text-h3 q-mb-lg font-poppins">Skills</h2>
          <p class="text-h6 font-inter q-mb-xl">
            I have experience building apps with .Net and Vue.js.<br> I am also familiar with database design and API development. <br> I am currently learning Quasar, in-fact this website is built with Quasar!  
          </p>
        </div>
      </div>
    </div>

    <!-- Contact section with background -->
    <div class="contact-section text-white q-pa-xl" :style="contactSectionStyle">
      <!-- Dark overlay for better text readability -->
      <div class="contact-overlay"></div>
      <div class="row justify-center" style="position: relative; z-index: 2;">
        <div class="col-12 col-md-8 text-center">
          <h2 class="text-h3 q-mb-lg font-poppins">Contact</h2>
          <p class="text-h6 font-inter q-mb-xl">
            Located in Minneapolis metro area!<br> Give me a shout!
          </p>
          
          <!-- Email Contact Button -->
          <q-btn
            color="white"
            text-color="white"
            size="lg"
            icon="mail"
            label="Send me an Email"
            href="mailto:cong.ha.cch@gmail.com"
            class="q-px-xl contact-btn"
            outline
          />
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import { computed } from 'vue'
import backgroundImage from 'assets/Background.jpg'
import aboutImage from 'assets/About.jpg'
import skillsImage from 'assets/Skills.jpg'
import contactImage from 'assets/Contact.jpg'
import resumePdf from 'assets/CongHa-2025-D-JUN.pdf'

// About section background style
const aboutSectionStyle = computed(() => ({
  backgroundImage: `url(${aboutImage})`,
  backgroundSize: 'cover',
  backgroundPosition: 'center center',
  backgroundRepeat: 'no-repeat',
  minHeight: '400px',
  position: 'relative'
}))

// Skills section background style
const skillsSectionStyle = computed(() => ({
  backgroundImage: `url(${skillsImage})`,
  backgroundSize: 'cover',
  backgroundPosition: 'center center',
  backgroundRepeat: 'no-repeat',
  minHeight: '400px',
  position: 'relative'
}))

// Contact section background style
const contactSectionStyle = computed(() => ({
  backgroundImage: `url(${contactImage})`,
  backgroundSize: 'cover',
  backgroundPosition: 'center center',
  backgroundRepeat: 'no-repeat',
  minHeight: '400px',
  position: 'relative'
}))
</script>

<style scoped>
/* Custom parallax with controlled image size */
.custom-parallax {
  background-color: #000000;
}

/* Override the parallax background image sizing */
.custom-parallax :deep(.q-parallax__media) {
  background-size: 60% auto !important;
  background-position: center center !important;
  background-repeat: no-repeat !important;
}

/* Responsive image sizing */
@media (max-width: 768px) {
  .custom-parallax :deep(.q-parallax__media) {
    background-size: 80% auto !important;
  }
}

@media (max-width: 480px) {
  .custom-parallax :deep(.q-parallax__media) {
    background-size: 95% auto !important;
  }
}

/* Dark overlay for parallax */
.parallax-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.4);
  z-index: 1;
}

/* About section styling */
.about-section {
  position: relative;
}

/* Dark overlay for about section */
.about-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  z-index: 1;
}

/* Skills section styling */
.skills-section {
  position: relative;
}

/* Dark overlay for skills section */
.skills-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  z-index: 1;
}

/* Contact section styling */
.contact-section {
  position: relative;
}

/* Dark overlay for contact section */
.contact-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  z-index: 1;
}

/* Ensure text appears above overlay */
.absolute-full > div {
  z-index: 2;
}

/* Contact button styling */
.contact-btn {
  transition: all 0.3s ease;
  font-weight: 600;
}

.contact-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 25px rgba(255, 255, 255, 0.3);
}
</style>
