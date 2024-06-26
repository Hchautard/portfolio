<template>
    <div class='homescreen-body'>
      <img src="../../public/assets/images/nuit_etoilee_wallpaper.jpg" id="wallpaper-painting">
      <div class="header">
        <div class="left-side">
          <h1><span>Hugo Chautard</span>Developpeur Web</h1>
        </div>
        <div class="right-side">
          <nav>
            <div class="me-title">
              <h1><a href="#about-me">projets,</a></h1>
            </div>
            <div class="project-title">
              <h1><a href="#my-projects">à propos,</a></h1>
            </div>
            <div class="contact-title">
              <h1><a href="#contact">contacter</a></h1>
            </div>
          </nav>
        </div>
      </div>
      <div class="text">
        <h1 class="big-title">Web</h1>
        <h1 class="big-title"><span>Designer</span> &</h1>
        <h1 class="big-title"><span>Developpeur</span> </h1>
        </div>
    </div>
</template>
  
  <script>
  export default {
    name: 'HomeScreen',
    data() {
      return {
        title: 'HomeScreen',
      }
    }
  }
  </script>
  
  <style lang="scss" scoped>
      @import "../../public/assets/css/const";

      @font-face {
        font-family: Agoka;
        src: url('../../public/assets/fonts/AgokaFamily.otf');
      }

      @font-face {
        font-family: Moderna;
        src: url('../../public/assets/fonts/MODERNA_.TTF');
      }

      .header {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 90%;
        margin: 0 auto;

        border-bottom: 2px solid rgba(245,238,230);    

        .left-side {
          h1 {
            font-size: 30px;
            font-family: 'Courier New', Courier, monospace;
            color: $white;
            margin-top: none;

            span {
              font-family: Agoka;
              font-size: 20px;
              color: $white;
              margin-left: 10px;
              margin-right: 20px;
            }
          }
        }

        .right-side {
          nav {
            font-family: 'Courier New', Courier, monospace;
            color: $white;
            display: flex;
            flex-direction: row;
            align-items: left;
            width: 27em;

            a {
              color: $white;
              text-decoration: none;
            }
          }
        }
      }
  
        .homescreen-body {
            // background-image: url('../../public/assets/images/nuit_etoilee_wallpaper.jpg');
            background-size: cover;
            background-repeat:no-repeat;
            // opacity: 0.6;
            height: 100vh;

            // animation: backgroundTransition 5s ease-in-out;
        }

        // @keyframes backgroundTransition {
        //     0% {
        //         background-image: url('../../public/assets/images/nuit_etoilee_wallpaper.jpg');
        //     }
        //     100% {
        //         background-image: none;
        //     }
        // }

        @font-face {
          font-family: 'Notted';
          src: url('../../public/assets/fonts/Notted.ttf');
        }

        @font-face {
          font-family: 'Rimogles';
          src: url('../../public/assets/fonts/Rimogles.ttf');
        }

        .text {
          padding-top: 220px;
            padding-left: 80px;
        }

        h1.big-title {
            font-family: Rimogles;
            font-size: 50px;
            color: $white;
            margin-top: 0;
            margin-bottom: -40px;
            

            span {
                color: $white;
                font-size: 200px;
            }
        }

        #wallpaper-painting {
          position: absolute;
          width: 198vh; 
          height: 100%;
          z-index: -1;
          opacity: 0.6;
        }

        .left-side, .right-side, .text {
          opacity: 1;
        }
  </style>
  