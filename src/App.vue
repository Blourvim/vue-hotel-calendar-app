<template>
<div id="wrapper">
<SideNavigation/>
<BigCalendar/>
<RightSideCalendar/>
</div>
</template>
<script>
import BigCalendar from './components/Calendar/BigCalendar.vue';
import SideNavigation from './components/SideNavigation.vue'
import RightSideCalendar from './components/RightSideCalendar/Calendar.vue'
 export default{
     name:'App',
     components:{
BigCalendar,
SideNavigation,
RightSideCalendar
     },
     data() {
      return {
          rooms : []
      }
    }
 }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400;1,500;1,700&display=swap');
:root {
--primary-highlight: #5372E7;
--secondary-text: #B9B9B9;
--faded-secondary-text :#D7D7D7;
--appointment-background:#E4F2F5;
--primary:#FAFAFA;
--secondary:#FFFFFF
}
body{
    padding:0;
    margin:0;
    font-family: 'DM Sans', sans-serif;}
#wrapper{
    display:flex;

}
</style>