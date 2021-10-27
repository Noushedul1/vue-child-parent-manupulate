<template>
  <p>{{fname}}</p>
  <button @click="add()">hello</button>
  <ComNewprops 
    :firstname="firstName"
    :secondname="secondName"
    :age="agE"
    @updateValue = "agE = $event"
    @updateNamevalue = "firstName = $event"
  />
  
  <form v-on:submit.prevent>
    <input type="text" v-model="myformdata.fname">
    <input type="number" v-model="myformdata.num">
    <input type="submit">
  </form>
  <p>{{myformdata.fname}}</p>
  <p>{{myformdata.num}}</p>
</template>
<script>
import ComNewprops from './components/Newprops.vue';
  export default{
    components: {
      ComNewprops
    },
    data(){
      return{
        fname: 'akib',
        food: [1,2,3,4],
        myformdata: {
          fname: '',
          num: ''
        },
        firstName: 'Noushedul',
        secondName: 'islam',
        agE: 25
      }
    },
    methods: {
      add(){
        this.fname = 'noushedul islam';
      },
      formdata(){
        `${this.myformdata} and ${this.myformdata}`;
      }
    }
  }
</script>
