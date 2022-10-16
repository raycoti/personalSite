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
              I am a Frontend developer with 4+ years of experience
              I specialize in Javascript/Typescript, React, Redux, and Node.
            </p>
            <p>
              I am from Chicago's beautiful Back of the Yards neighborhood
              where I developed my love of art and technology. My fascination with software
              development was sparked by the desire to learn how people built educational
              games that I spent countless hours on.
              Now I am happy to work in the EdTech industry!
              Outside of coding I enjoy dancing, drawing, and cooking.
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
