<template>
    
     <div class="iphonebox">
         
        <div v-for="iphone in iphone" :key="iphone.id" >
                
                <Iphone :iphone="iphone"/>
        </div>

        

     </div>

</template>

<script>

import Iphone from "./Iphone.vue"
export default{
    //eslint-disable-next-line
    name: 'Iphonebox',
    components: {
        Iphone
    },
    props: {
        iphone: Array
    }

}

</script>


<style>

.iphonebox{

    padding: 40px;
    color: gray;
    grid-template-columns: 1fr 1fr 1fr;
    border:3px solid rgb(29, 70, 127);
    background-image: url("https://w0.peakpx.com/wallpaper/590/496/HD-wallpaper-apple-iphone-apple-logo-blur-iphone-6-iphone-7-iphone-8-iphone-x-logo-thumbnail.jpg");
    background-repeat: no-repeat;
    background-attachment: fixed;  
    background-size: cover;
}
</style>