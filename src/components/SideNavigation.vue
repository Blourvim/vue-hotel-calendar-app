<template>
    <div id='side-navigation'>
        <div id='hotel-card'>
<div id='hotel-avatar'>
<h3>PH</h3>
</div>
    <div id='hotel-card-text'>
<p>Paradise</p>
<p>Hotel</p>

    </div>
        </div>
    <nav>
<button><img src="../assets/Rooms.svg" alt="sad"/>Yönetim Paneli</button>
<button id='current-tab'><img src="../assets/Room.svg" alt="sad"/>Odalar</button>
<button><img src="../assets/Social.svg" alt="sad"/>Topluluk</button>
<button><img src="../assets/Chat.svg" alt="sad"/>Mesajlar</button>
<button><img src="../assets/Statistics.svg" alt="sad"/>İstatistikler</button>

    </nav>
    </div>

</template>

<script>
export default{
    name:'SideNavigation',
}
</script>

<style scoped>
#side-navigation{
background: var(--secondary);
height:100vh;
width: 15%;
}
#hotel-avatar{
    background:var(--primary-highlight);
    width: 2.5em; height: 2.5em;
    border-radius: 50%;
    margin:1em
}
h3{
    color:var(--secondary);
    text-align: center;
    vertical-align: middle;
    line-height: 0.3rem;   
    font-weight: 400;
}
#hotel-card{
    display:flex
}
#hotel-card-text{
color:#6479C0;
    margin-top:1em

}
p{
margin:0;
padding-bottom: 3px;
}
nav{
    display: -ms-inline-grid;
    display: inline-grid;
    margin-left: 1.5em;
    margin-top:2em;
}
button{
    margin-bottom: 2em;
    border:none;
    padding:1em;
    border-radius:10px;
    cursor:pointer;
    background:var(--secondary)

}
button :hover{
}
#current-tab{
    background:var(--primary-highlight);
    color:var(--secondary)
}
</style>