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
<div><img src="../assets/Rooms.svg" alt="sad"/>Yönetim Paneli</div>
<div id='current-tab'><img src="../assets/Room.svg" alt="sad"/>Odalar</div>
<div><img src="../assets/Social.svg" alt="sad"/>Topluluk</div>
<div><img src="../assets/Chat.svg" alt="sad"/>Mesajlar</div>
<div><img src="../assets/Statistics.svg" alt="sad"/>İstatistikler</div>

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
    margin:1em;
}
h3{
    color:var(--secondary);
    text-align: center;
    vertical-align: middle;
    line-height: 0.3rem;   
    font-weight: 400;
}
#hotel-card{
    display:flex;
    margin-top:1.5em

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
nav div{
    margin-bottom: 1em;
    border:none;
    padding:0.5em;
    border-radius:10px;
    cursor:pointer;
    background:var(--secondary);
    color:var(--secondary-text)

}

#current-tab{
    background:var(--primary-highlight);
    color:var(--secondary)
}
img{
    margin-right: 1em;
    margin-bottom: -0.2em;
}
</style>