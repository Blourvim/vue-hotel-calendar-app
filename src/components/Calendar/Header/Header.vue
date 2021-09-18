<template>
  <header>
    <h3>
Odalar
    </h3>
    <a id="sayı">9</a>
    <a>Boş Oda</a>
<SearchBar/>

      </header>
</template>

<script>
import SearchBar from './SearchBar.vue';
export default {
name:'Header',
components:{
  SearchBar
}
}
</script>

<style scoped>
header{
  font-size:1.5em;
  display:flex;
  margin-top:2em;
  position:relative;
  height: 4em;
}
#sayı{
  color: var(--primary-highlight);
}
a{
  margin-top:  0.7em;
  margin-right: 0.4em;
  font-size: 70%;
  font-weight: 400;
  color:var(--secondary-font)
}
h3{
  font-weight: lighter;
  margin-top: 0%;
  margin-left:4% ;
  margin-right:4% ;
  color:rgb(59, 59, 58)

}
</style>