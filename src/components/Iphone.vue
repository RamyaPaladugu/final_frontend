<template>

<div class = "float-container">
    <div class="iphone">
        <ul><h1 style="color:cadetblue">{{iphone.iphoneModel}}</h1></ul>
        <ul><h4>Price : {{iphone.price}}</h4></ul>
        <ul><h4>Camera Pixel : {{iphone.cameraPixel}}</h4></ul>
        <ul><h4>Released Year :  {{iphone.releasedYear}}</h4></ul>
        <ul><h4 v-if="iphone.inMarket === true">Still in Market : Yes</h4>
        <h4 v-else>Still in Market : No</h4></ul>
        <button @click="toggle">colors</button>
        <div v-if="active">
            <img :src="`${iphone.image}`" width="100" height="100"/>
        </div>
    </div>
    </div>
</template>

<script>

export default{
    //eslint-disable-next-line
    name: 'Iphone',
    props:{
        iphone: Array
    },
    data () {
      return {
        active: false
      }
    },
    methods: {
      toggle () {
        this.active = !this.active
      }
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

button{
    border-radius: 20px;
    width: 20%;
    font-size: 20px;
    background-color: #8B9D83;
    color: black;
}

.iphone{
    background-color: #e3e6ec;
    color:rgb(60, 86, 135);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width:60%;
    border-radius: 20px;
}

.colors
{
    background-color: white;
    color:rgb(60, 86, 135);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    border-radius: 20px;
}
button:hover {
 border: 5px solid;
 color: black;
 box-shadow: 8px 8px rgb(110, 125, 197);
}
.iphone:hover {
 border: 5px solid yellow;
 color: rgb(53, 182, 152);
 box-shadow: 8px 8px rgb(110, 125, 197);
}
.colors:hover {
 border: 5px solid yellow;
 color: rgb(53, 182, 152);
 box-shadow: 8px 8px rgb(110, 125, 197);
}
.float-container {
    display: flex;
}



</style>