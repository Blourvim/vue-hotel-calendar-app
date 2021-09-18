<template>
  <header>
    <a>
ODALAR
    </a>
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
  margin-top:  0.4em;
}
</style>