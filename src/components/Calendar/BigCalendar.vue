<template>
  <div id="calendar">
    <Header/>
 <CalendarLine/>


  </div>
</template>

<script>
import Header from './Header/Header.vue';
import CalendarLine from './CalendarLine.vue'
export default {
name:'BigCalendar',
components:{
  Header,
  CalendarLine
},
 items: [
        { name: 'apple', price: '7' },
        { name: 'orange', price: '12' }
      ]
}
</script>

<style scoped>
#calendar{
      background:var(--primary);
  width:60%;
}
</style>