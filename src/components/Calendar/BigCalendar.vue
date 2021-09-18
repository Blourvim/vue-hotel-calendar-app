<template>
  <div id="calendar">
    <Header/>
<CalendarLine/>
  </div>
</template>

<script>
import CalendarLine from './CalendarLine.vue';
import Header from './Header/Header.vue';
export default {
name:'BigCalendar',
components:{
  CalendarLine,
  Header
}
}
</script>

<style scoped>
#calendar{
      background:var(--primary);
  width:60%;
}
</style>