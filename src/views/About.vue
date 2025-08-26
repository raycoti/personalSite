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
              Howdy y'all! I am a Frontend developer with 8+ years of frontend developer
              experience who specializes in Typescript and React.
              When I'm not working i'm either cooking up some food,
              dancing or working on an art project
            </p>
            <p>
              I was born and raised in Chicago, originating from the beautiful Back of the Yards
              neighborhood where I developed my love of art and the city.
              My fascination with software development was sparked by the desire to learn how people
              built the educational computer games that I spent countless hours on as a child.
              My first coding project was a math quiz game, and in a full circle moment
              I am proud to say that I work in the EdTech industry!
            </p>
            <p>
              This site mostly contains my art work
              using a combination of 3D modeling (Blender) and digital drawing (Procreate).
              NO AI HERE.
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

import Ray from '@/assets/ray.jpeg';
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
