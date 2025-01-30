<template>
    <v-container id="hero-image" fluid>
      <v-row>
        <v-col cols="12" md="6">
          <img class="sideimag" :src="require('../assets/hero,sideimag.png')" alt="Side Image" />
        </v-col>
        <v-col cols="12" md="6" class="text-container">
          <h2 id="headline">velkommen til min verden</h2>
          <h1>Mit navn er Shahad,</h1>
          <h1>og jeg er <span>Webudvikler</span></h1>
          <h2 id="changingH2">{{ currentText }}</h2>
          <div class="icons">
            <a href="https://github.com/Shahad1991">
              <img :src="require('../assets/github.svg')" alt="GitHub icon" />
            </a>
            <a href="https://www.instagram.com/shahadnazaromhassoni/">
              <img :src="require('../assets/Vector.svg')" alt="Instagram icon" />
            </a>
            <a href="https://www.linkedin.com/in/shahad-al-jawashee-41502a24b/">
              <img :src="require('../assets/linkdin.svg')" alt="LinkedIn icon" />
            </a>
          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" class="hero-img-container">
          <img class="hero-img" :src="require('../assets/myimag.png')" alt="Hero image" />
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'HeroImage',
    data() {
      return {
        h2Texts: ['kreativ', 'samarbeidsvillig', 'nysgerrig', 'struktureret', 'ambitiøs', 'detaljeorienteret', 'imødekommende'],
        currentIndex: 0,
        letterIndex: 0,
        currentText: '',
      };
    },
    mounted() {
      this.typeWriter();
    },
    methods: {
      typeWriter() {
        if (this.letterIndex < this.h2Texts[this.currentIndex].length) {
          this.currentText += this.h2Texts[this.currentIndex].charAt(this.letterIndex);
          this.letterIndex++;
          setTimeout(this.typeWriter, 100);
        } else {
          setTimeout(this.eraseText, 1000);
        }
      },
      eraseText() {
        if (this.letterIndex > 0) {
          this.currentText = this.currentText.slice(0, -1);
          this.letterIndex--;
          setTimeout(this.eraseText, 50);
        } else {
          this.currentIndex = (this.currentIndex + 1) % this.h2Texts.length;
          setTimeout(this.typeWriter, 300);
        }
      },
    },
  };
  </script>
  
  <style scoped>
  #hero-image {
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 70px;
    height: 500px;
  }
  
  .sideimag {
    width: 100%;
    height: auto;
  }
  
  .text-container {
    width: 70%;
    margin-left: 20px;
  }
  
  .hero-img-container {
    width: 50%;
    display: flex;
    justify-content: flex-end;
  }
  
  .hero-img {
    position: relative;
    z-index: 1;
    max-width: 100%;
    height: auto;
    border-radius: 200px 200px 30px 30px;
    border-bottom: 5px;
  }
  
  .icons img {
    width: 30px;
    margin-top: 15px;
    margin-right: 10px;
    height: auto;
    transition: transform 0.3s ease;
  }
  
  .icons img:hover {
    transform: scale(1.2);
    background-image: linear-gradient(90deg, #FFEAC2, #EED5A2, #745D29);
  }
  
  .icons a {
    margin-right: 15px;
  }
  </style>