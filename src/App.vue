<script>
export default {

    data(){
        return {

        }
    },
    components: {
        
    },
    props: {
        
    },
    methods: {
      openWindow(_window){
        window.open(`https://${_window}.jonx.dev`, '_blank');
      },
    },
    created() {
        
    },
    mounted(){
        
    },
    watch: {
        
    },

}
</script>

<template>
  <div id="wrapper" class="unmarkable">
    <h1 id="header">Welcome to Jonx.dev</h1>

    <div id="mainContainer">
      <h2>My Projects</h2>
      <div id="projectContainer">
        <div class="projectWrapper clickable" @click="openWindow('portfolio')">
          <h3>Portfolio</h3>
          <img src="./assets/portfolio.png">
        </div>
        <div class="projectWrapper clickable"  @click="openWindow('spotify')">
          <h3>spotify playlist editor</h3>
          <img src="./assets/spotify.png">
        </div>
        <div class="projectWrapper clickable"  @click="openWindow('lichtbier')">
          <h3>Lichtbierrechner</h3>
          <img src="./assets/lichtbier.png">
        </div>

        
      </div>
    </div>
  </div>

</template>

<style scoped>
    #header{
      position: relative;

      width: 100%;
      background: linear-gradient(318deg, rgb(163, 42, 255) 0%, rgb(30, 192, 197) 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      font-size: 340%;
      text-align: center;
    }

    #mainContainer{
      position: absolute;
      left: 50%;
      transform: translateX(-50%);

      width: 70%;
      min-width: 1700px;
      height: 45%;
      min-height: 400px;

      background-color: rgba(255, 255, 255, 0.116);
      border-radius: 18px;
    }

    #mainContainer h2{
      text-align: center;
      font-size: 200%;
    }

    #projectContainer{
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
    }

    .projectWrapper{
      width: 460px;
      height: 200px;

      margin-bottom: 45px;
    }

    .projectWrapper h3{
      text-align: center;
      z-index: 1;
      
    }

    .projectWrapper img{
      width: 100%;
      position: relative;
      left: 50%;
      top:0%;
      transform: translateX(-50%);
      object-fit: contain;
      border-radius: 8px;
    }

    .clickable{
      cursor: pointer;
    }

    .unmarkable{
      -webkit-touch-callout: none;
      -webkit-user-select: none;
      -khtml-user-select: none;
      -moz-user-select: none;
      -ms-user-select: none;
      user-select: none;
    }

    @media (orientation: portrait) {
      #mainContainer{
        width: 80%;
        min-width: 0px;
        height: fit-content;
        min-height: none;
        padding: 10px;
        margin-bottom: 80px;
      }

      .projectWrapper{
        width: 80%;
        height: fit-content;
        margin-bottom: 30px;
    }
    }
    

    
</style>