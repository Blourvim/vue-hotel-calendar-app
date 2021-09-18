<template>
  <input placeholder="&emsp;&emsp;&emsp;Aramak istediğiniz metni yazınız" type='text'/>
  <img src="../../../assets/Magnify.svg" alt="">
</template>

<script>
export default {
name:'SearchBar'
}
</script>

<style scoped>
input{
    height:3em;
    border:none;
    border-radius: 10px;
    width: 45%;
     position:absolute;
     right:0;
     margin-right: 2em;
     margin-top:0%;
}

img{
  height:1.2rem;
  width:1.2rem;
  position: absolute;
    right:45%;
    margin-top: 0.8rem;
}
</style>