<script>
import Blog from './components/Blog.vue';
import Photo from './components/Photo.vue';
import Projects from './components/Projects.vue';

export default {

  data(){
    return {
      view: "main",
    }
  },
    components: {
      Blog,
      Photo,
      Projects,
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
 <div class="window" id="mainView" v-if="view === 'main'">
  <div id="wrapper" class="unmarkable">
    <div id="navBar">
      <h1 class="navBarButton">Blog</h1>
      <h1 class="navBarButton" @click="view = 'photo'">Photography</h1>
      <h1 class="navBarButton">Projects</h1>
    </div>
    <h1 id="MainText">Welcome to Jonx.dev</h1>
  </div>
 </div>

 <div class="window" id="photoView" v-else-if="view === 'photo'">
  <Photo></Photo>
 </div>

</template>

<style scoped>
    #navBar{
      width: 100%;
      height: 60px;

      display: flex;
      justify-content: space-evenly;
    }

    .navBarButton{
      padding-bottom: 40px;
      margin-top: 15px;
    }

    .navBarButton:hover{
      cursor: pointer;
      border-bottom: 4px solid white;
      
    }

    #MainText{
      position: absolute;

      background: linear-gradient(318deg, rgb(163, 42, 255) 0%, rgb(30, 192, 197) 100%);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      line-height: normal;
      font-size: 7rem;
      width: 100%;
      text-align: center;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      margin: 0;
    }

    #mainContainer{
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);

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

        position: static;
        transform: translateX(0);
        margin-left: calc(10% - 10px);
      }

      .projectWrapper{
        width: 80%;
        height: fit-content;
        margin-bottom: 30px;
    }
    }
    

    
</style>