<template>
  <div id="profile">
      <div id='buttons'>
          
      <img src="../../assets/Chat.svg" alt="chat">
      <img src="../../assets/Notification.svg" alt="notification">
      </div>
      <div id="profile-bar">
          <img id='profile-img' src="https://picsum.photos/40/40" alt="profile-picture">
     <div id="proile-texts"> 
        <p>Esra İzen</p>
        <p>Resepsiyon</p>
     </div>
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
    width:9rem;
    margin: 2rem;
    border-radius: 10px;
    padding:0.7rem;

}
p{
    padding: 0%; margin:0%;
}
#profile-img{
    width:2rem;height:2rem;
    margin:0.5rem;
    margin-right: 1rem;

}
#buttons{
margin-top: 3rem;
justify-items:space-between;
}

#button-image{
    height:2rem; width:2rem;
}
</style>
