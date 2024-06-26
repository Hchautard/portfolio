<template>
    <div id="about-me">
      <img src="../../public/assets/images/monet.jpg" id="wallpaper-painting-2">
      <div id="about-me-section">
        <div id="about-me-image">
              <img src="../../public/assets/images/magueule_sans_septum.jpg" alt="me">
          </div>
          <div id="about-me-text">
              <h3>Enchanté, moi c'est Hugo </h3>
              <p>
                Je suis un développeur fullstack junior basé dans le sud de la France, originaire de Saint Rémy de Provence. 
                J'ai une passion pour l’art et je suis toujours prêt à explorer de nouvelles façons d'intégrer le design dans mes projets numériques.
              </p>
              <div id="about-me-link">
                <a href="https://www.linkedin.com/in/hugo-chautard-409a151a0/" target="_blank">LinkedIn</a>
                <br>
                <a href="https://github.com/SuhDud3" target="_blank">Github</a>
                <br>
                <a href="">chautardhugo@gmail.com</a>
              </div>
          </div>
      </div>
    </div>
</template>
  
  <script>
  export default {
    name: 'AboutMe',
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style lang="scss" scoped>
        @import "../../public/assets/css/const.scss";

        @font-face {
          font-family: 'Notted';
          src: url('../../public/assets/fonts/Notted.ttf');
        }

        @font-face {
          font-family: 'Rimogles';
          src: url('../../public/assets/fonts/Rimogles.ttf');
        }

        @font-face {
        font-family: Agoka;
        src: url('../../public/assets/fonts/AgokaFamily.otf');
        }

        @font-face {
          font-family: Moderna;
          src: url('../../public/assets/fonts/MODERNA_.TTF');
        }


      h1 {
          margin-bottom: 40px;
      }

      #about-me {
          display: flex;
          flex-direction: column;
          justify-content: space-around;
          align-items: center;
          // background-image: url('../../public/assets/images/monet.jpg');
          height: 100vh;
      }

      #wallpaper-painting-2 {
          position: absolute;
          width: 209vh; 
          height: 100%;
          z-index: -1;
          // opacity: ;
        }
  
      #about-me-section {
        width: 60%;
        display: flex;
        background-color: $white;
        border-radius: 20px;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 14px 28px, rgba(0, 0, 0, 0.22) 0px 10px 10px;
      }

      #about-me-text, #about-me-image {
          margin: 20px;
      }

      #about-me-text {
          width: 50%;
          margin-left: 7%;

          h3 {
              font-family: 'Notted';
              font-size: 3em;
              color: $darkDarkColor;
          }

          p {
              font-family: monospace;
              font-size: 1.5em;
              font-weight: 300;
              color: $darkDarkColor;
              text-align: justify;
              line-height: 1.5em;
          }
      }

      #about-me-link {
          margin-top: 20px;

          a {
              font-family: 'Courier New', Courier, monospace;
              color: $darkDarkColor;
              text-decoration: none;
          }
      }

      
      img {
          float: left;
          width: 20em;
          margin: 10px;
          border-radius: 20px;
      }

      p {
          text-align: justify;
      }
      

  </style>
  