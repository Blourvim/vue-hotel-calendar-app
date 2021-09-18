<template>
  <div id="profile">
      <div id='buttons'>
          
      <img class="button-image" src="../../assets/Chat.svg" alt="chat">
      <img class='button-image' src="../../assets/Notification.svg" alt="notification">
      </div>
      <div id="profile-bar">
          <img id='profile-img' src="../../assets/Ellipse.png" alt="profile-picture">
     <div id="proile-texts"> 
        <p>Esra İzen</p>
        <a>Resepsiyon</a>
     </div>
        <img id='half-arrow' src="../../assets/Half-Arrow.svg" alt="">

      </div>
  </div>
</template>

<script>
import '../../assets/Chat.svg'
export default {
name:'Profile'
}
</script>

<style scoped>

#profile{
    display:flex;

}
#profile-bar{
    display: flex;
    background:var(--secondary);
        height:3rem;
    width:10rem;
    margin: 2rem;
    border-radius: 10px;
    padding:0.7rem;

}
p{
    padding: 0%; margin:0%;
}
a{
    color:var(--secondary-text);
    font-size:0.8rem;
}
#profile-img{
    width:2rem;height:2rem;
    margin:0.5rem;
    margin-right: 1rem;
    border-radius:50%;

}
#buttons{
margin-top: 3.5rem;
display: flex;
justify-content:space-between;
width:4rem
}

.button-image{
    height:1.2rem; width:1.2rem;
}
#half-arrow{
    margin-left:10px;
    margin-top:10%;
    height:1rem;width:1rem;
}
</style>
