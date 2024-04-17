<template>
    <div id="about-me">
    <div id="about-me-section">
      <div id="about-me-image">
            <img src="../../public/assets/images/magueule_sans_septum.jpg" alt="me">
        </div>
        <div id="about-me-text">
            <h3>Salut, moi c'est Hugo </h3>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis reiciendis aut accusantium quaerat alias explicabo doloribus sapiente, dolorum cum numquam nobis debitis, quidem vitae obcaecati dicta corporis aliquid adipisci earum.
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Laudantium doloremque veritatis vel reiciendis pariatur, quibusdam unde! Voluptatum, culpa vero? Cum reprehenderit quaerat necessitatibus nam officiis nostrum odio hic doloremque pariatur!
            </p>
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

      h1 {
          margin-bottom: 40px;
      }

      #about-me {
          display: flex;
          flex-direction: column;
          justify-content: space-around;
          align-items: center;
            margin: 100px;
      }
  
      #about-me-section {
        width: 100%;
        display: flex;
        justify-content: center;
      }

      #about-me-text, #about-me-image {
          margin: 20px;
      }

      
      img {
          float: left;
          width: 20em;
          margin: 10px
      }

      p {
          text-align: justify;
      }
      

  </style>
  