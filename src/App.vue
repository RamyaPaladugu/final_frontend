<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header class="header" TitleName="IPHONE COLLECTION"  />



    <Iphonebox :iphone="iphone"  />
    <div class="About">
    <h1> <button><a href="https://vueprojectfinal.herokuapp.com/"> <i> For exiciting offers click here !! </i></a></button> </h1>

    </div>


  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import Iphonebox from './components/Iphonebox.vue'



// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Iphonebox
  },

  data(){
    return {
      iphone: []
    }
  },
  methods: {
    // promises

      async fetchstudent(){
         const res= await fetch('https://vueprojectfinal.herokuapp.com/api')
         const data= await res.json()
          console.log("Hello",data[0].Iphone)
         return data[0].Iphone
      }

  },

  async created(){
    this.iphone = await this.fetchstudent()
    console.log("Hello1",typeof(this.iphone))
    console.log("here is",this.iphone)
  }
}
</script>










<style>


@import url('https://fonts.googleapis.com/css?family=Tangerine:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0px;
}
.header
{
  background: black;
  background-color: #274156;
}
body {
  font-family: 'Courier New', monospace;
}
.container {
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 40px;
  border-radius: 5px;
  width:100%;
  background-color: #D0CCD0;
  

}

div{
  margin-bottom: 0.5em;
  padding:10px;
}
.About{
  width:100%;
}
a{
    text-decoration: none;
    color: rgb(2, 7, 16);

}
button{
    font-size:30px;
    font-family:'Times New Roman', Times, serif;
    background-color: rgb(193, 218, 224);
    width:100%;
    border:3px solid rgb(46, 99, 173);


}



</style>


