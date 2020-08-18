<template>
  <div >
    <button @click="upFunction" class="btn btn-info">{{ Start }}</button>
    <p v-bind:style="{ fontSize: fsize + 'px' }">{{ counter }}</p>
   
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fsize: 50,
      player:[
          {name:'A', hp:100 , image: './assets/Anakin.jpg'},
          {name:'D', hp:300 , image: './assets/Doraemon.jpg'},
          {name:'Ir', hp:100 , image: './assets/Ir.jpg'},
      ],
      monster:[
          {name:'A', hp:100 , image: ''},
          {name:'A', hp:100 , image: ''},
          {name:'A', hp:100 , image: ''},
      ]
        
      
    };
  },

  props: {
    Start: String,
    End: String,
    
  },

  methods: {
    upFunction: function () {
      this.counter += 1;
      this.fsize += 10;

      //console.log('fsize =' +this.fsize);
      //console.log('counter =' +this.counter);

      //ส่งค่าตัวแปร counter ออกไปโดยผ่านตัวแปร cc
      this.$emit('cc',this.counter)

    },

    downFunction: function () {
      this.counter -= 1;
      this.fsize -= 10;

      console.log(this.fsize);
      console.log(this.counter);
    },
  },
};
</script>


<style>
</style>
