<!-- FILEPATH: /home/cc3sar/MyProjects/Portfolio/src/views/About.vue -->

<template>
  <div id="about">
    <h1 class="principal-text">
      <span class="font-white">
        - About
      </span>
      <span class="font-violet">
        me
      </span>
    </h1>
    <br>
    <article class="about-me">
      <section>
        <p class="font-white about-me-information">
          I am currently a fourth-year student pursuing a degree in Systems Engineering. 
          As an aspiring engineer, I have developed a strong passion for programming and technology. 
          My journey in the world of software development has been driven by a love for problem-solving and creating innovative solutions. 
          One of my greatest passions outside of the tech world is my love for dogs. 
          I am an avid dog lover and cherish the companionship and joy they bring to my life. 
          In my free time, you'll often find me spending quality time with my own beloved dogs, going for long walks, 
          playing fetch, and simply enjoying their company. In terms of programming, I have gained valuable experience in various technologies and frameworks. 
          I am proficient in Next.js and React, using them to build modern and responsive web applications. 
          Additionally, I have worked extensively with Python, Django, and Django Rest Framework, crafting robust and scalable backend systems. 
          I also have expertise in implementing electronic signature solutions and integrating secure credit card payment systems.
        </p>
        <div class="about-images-container">
          <ul class="carousel">
            <li v-if="currentImage === 0">
              <img src="https://via.placeholder.com/150x150.png?text=Image+1" alt="Image 1">
            </li>
            <li v-if="currentImage === 1">
              <img src="https://via.placeholder.com/150x150.png?text=Image+2" alt="Image 2">
            </li>
            <li v-if="currentImage === 2">
              <img src="https://via.placeholder.com/150x150.png?text=Image+3" alt="Image 3">
            </li>
          </ul>
          <div class="carousel-buttons">
            <button class="carousel-button" @click="prevImage">Prev</button>
            <button class="carousel-button" @click="nextImage">Next</button>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style scoped>
  .about-images-container {
    background-color: #2F3B47;
    height: 200px;
    overflow: hidden;
    position: relative;
  }

  .carousel {
    /* display: flex; */
    list-style: none;
    /* margin: 0;
    padding: 0; */
    /* width: 98%;
    height: 98%; */
  }

  .carousel li {
    display: flex;
    flex-direction: column;
    align-items: center;
    /* justify-content: center; */
  }

  .carousel img {
    /* display: block; */
    /* height: 195px; */
    /* object-fit: cover; */
    width: 98%;
    height: 195px;
    /* margin-top: -10px; */
    /* margin-left: -10px; */
    /* margin: auto; */

  }

  .carousel-buttons {
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
  }

  .carousel-button {
    background-color: #fff;
    border: none;
    color: #2F3B47;
    cursor: pointer;
    font-size: 16px;
    margin-right: 10px;
    padding: 10px;
  }
</style>

<script>
export default {
  data() {
    return {
      currentImage: 0,
      totalImages: 3
    }
  },
  methods: {
    prevImage() {
      this.currentImage = (this.currentImage - 1 + this.totalImages) % this.totalImages;
    },
    nextImage() {
      this.currentImage = (this.currentImage + 1) % this.totalImages;
    }
  }
}
</script>