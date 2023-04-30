<template>
<div>
    <h1> {{TitleName}} </h1>

</div>
</template>

<script>

export default{
  // eslint-disable-next-line 
    name: 'Header',
    props:{
        TitleName: String
    }
}

</script>

<style scoped>

div{
    text-align: center;
    color: white;
    font-family: 'Times New Roman', Times, serif;
}

</style>