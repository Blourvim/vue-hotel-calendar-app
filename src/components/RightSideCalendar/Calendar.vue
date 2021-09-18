<template>
<div id='wrapper'>
<Profile/>
    <div>
<flat-pickr class="form-control"
                          :config="configs.inline"
                          v-model="form.dateInline">
              </flat-pickr>
    </div>
    </div>
</template>

<script>
    import flatPickr from 'vue-flatpickr-component';
    import 'flatpickr/dist/flatpickr.css';
    import Profile from './Profile.vue';
    export default {
        data() {
            return {
                 form: {
        dateBasic: null,
        dateTime: null,
        time: null,
        date: '2017-01-01',
        dateLocale: null,
        dateInline: +new Date(),
        dateConfirm: null,
        allowInput: null,
        dateStart: null,
        dateEnd: null,
        monthSelect: null,
      },
                date: null,
                configs:{
                    inline:{
                        inline:true
                    }
                }
            }
        },
        components: {
            flatPickr,
            Profile
        },
    }
</script>

<style scoped>
#wrapper{
    display:block;
    background:var(--primary)
}
</style>