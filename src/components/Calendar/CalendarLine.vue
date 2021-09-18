<template>
  <body>
      <div class="container">
        <div class="item" v-for="(room, index) in computed_items" :key="index">
          <div class="rooms">
            ODA {{index+1}}
          </div>
        </div>
      </div>

          <button class="add-button" @click="storeroom">
          Oda Ekle
        </button>
    
  </body>
</template>

<script>
export default {
  name: "roomApp",
  data(){
    return {
      room: "",
      priority: "",
      rooms: [],
      roomDesc:"",
      category:"",
      removedrooms: [],
      isError: false,
      isErrorNum: false,
      selectedCategory: ""
    }
},
  computed: {
    computed_items: function () {
        if(this.selectedCategory!=="") {
            let filtertype = this.rooms.filter((a)=>{
            if(a.cat === this.selectedCategory){
             return a;
          } 
        }) 
        return filtertype;
        } else {
          return this.rooms;
        }
      },
      
      dropDown() {
        let arr= [];
        this.rooms.forEach((e) => {
          arr.push(e.cat);
        });
        let unique = arr.filter((item, i, ar) => ar.indexOf(item) === i);
          return unique;
      }
    },
  methods: 
  {
    validateNumber()
      {
        let keyCode = event.keyCode;
        if(keyCode < 48 || keyCode > 57)
        {
          event.preventDefault();
          this.isErrorNum = true
          // alert("Please enter num");
          // document.getElementById("output-box").innerHTML += "Sorry! <code>preventDefault()</code> won't let you check this!<br>";
        }
        else{
          this.isErrorNum = false
        }
      },
    storeroom() 
    {
    
        this.rooms.push({name: this.room, desc:this.roomDesc, cat:this.roomCat, seq:Number(this.priority), isStrikedOff: false});
      
     
    },
    removeroom(index) 
    {
      this.removedrooms.push(...this.rooms.splice(index, 1));
    },
    deleteroom(index) 
    {
      this.removedrooms.splice(index,1)
    },
    doneroom(index)
    {
        this.rooms[index].isStrikedOff=true;
    },
    retrieveroom(index)
    {
      this.rooms.push(...this.removedrooms.splice(index, 1));
      this.rooms.sort( (a, b) => { return a.seq - b.seq} )
    }
  },
  
  
  mounted() 
  {
    console.log('App mounted!');
    if (localStorage.getItem('rooms')) this.rooms = JSON.parse(localStorage.getItem('rooms'));
    if (localStorage.getItem('removedrooms')) this.removedrooms = JSON.parse(localStorage.getItem('removedrooms'));
  },
  watch: 
  {
    rooms: 
    {
      handler() 
      {
        console.log('rooms changed!');
        localStorage.setItem('rooms', JSON.stringify(this.rooms));
      },
      deep: true,
    },
    removedrooms: 
    {
      handler() 
      {
        console.log('rooms changed!');
        localStorage.setItem('removedrooms', JSON.stringify(this.removedrooms));
      },
      deep: true,
    },
  },
};
</script>
<style scoped>

.add-button{
background:var(--primary-highlight);
height:2.3rem;
width:6rem;
border:none;
border-radius:10px;
color:var(--secondary);
margin-left:2rem;
margin-top:1rem
}
.rooms{
  color:var(--faded-secondary-text);
  font-size:1.2rem;
  margin-left:2em;
  padding-top:2em;
  border-bottom:solid var(--faded-secondary-text) 1px;
}
</style>