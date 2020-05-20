<template>
  <div class="about">
    <div class="center">
      <div class="container">
        <h1 class="title">ABOUT ME</h1>
        <div class="grid">
          <span class="ray">
            <img class="picture" :src="Ray" />
          </span>
          <span class="text">
            <p>
              I am a Fullstack developer with 3+ years of experience, currently working
              as the Lead Frontend Developer at Openfinance. During my tenure here, I led
              development of the Web App for the first US-regulated security token trading
              platform. Highlights of this experience include making contributions to our Apis,
              architecting a scalable React/Redux application
              and building npm packages for our Component Libraries and Sdks.
              I specialize in Javascript/Typescript, React, Redux and Node.
            </p>
            <p>
              I am from Chicago’s beautiful Back of the Yards neighborhood
              where I developed my love of art and technology. My facination with software
              development was sparked by the desire to learn how people built educational
              games like Math Blaster! and ClueFinders that I spent countless hours on.
              I hope to one day go full circle and work in EdTech!
              Outside of coding I enjoy dancing, drawing and cooking.
            </p>
          </span>
          <span class="bottom">
              <a
                target="_blank"
                href="https://www.linkedin.com/in/raycoti/">
                <img class="image" :src="Linkedin"/>
              </a>
              <a
                target="_blank"
                href="https://github.com/raycoti">
                <img class="image" :src="Git"/>
              </a>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Ray from '@/assets/ray.jpg';
import Linkedin from '@/assets/linkedin.png';
import Git from '@/assets/github.png';

export default {
  name: 'About',
  data: () => ({
    Ray,
    Linkedin,
    Git,
  }),
};
</script>
<style scoped lang="scss">
@import './About.scss';
</style>
