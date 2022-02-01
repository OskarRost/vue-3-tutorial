<template>
  <h3>Calculator</h3>
  <div>
    <input type="number" v-model="num1" />
    <input type="number" v-model="num2" />
  </div>
  <form v-on:submit.prevent="add">
      <div class="button-group1"> <button type="submit" class="button">+</button> </div>
  </form>
  <form v-on:submit.prevent="minus">
      <div class="button-group2"> <button type="submit" class="button">-</button></div>
  </form>
  <form v-on:submit.prevent="multiply">
      <div class="button-group3">  <button type="submit" class="button">*</button></div>
  </form>
  <form v-on:submit.prevent="geteilt">
      <div class="button-group4">  <button type="submit" class="button">÷</button></div>
  </form>
 

  
  
  
  <p>Result: {{ sum }}</p>
</template>
<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      sum: 0,
    };
  },
  methods: {
    add: function () {
      this.sum = parseInt(this.num1, 10) + parseInt(this.num2, 10);
    },
    minus: function () {
      this.sum = parseInt(this.num1, 10) - parseInt(this.num2, 10);
    },
    multiply: function () {
      this.sum = parseInt(this.num1, 10) * parseInt(this.num2, 10);
    },
    geteilt: function () {
      this.sum = parseInt(this.num1, 10) / parseInt(this.num2, 10);
    },
  },
};
</script>
<style>
 button {
	display:inline-block;
	height:40px;
	width:138px;
  margin: 10;
  padding: 10;   
  border: 1px solid;
  cursor: pointer;
  }

  .button-grop1, .button-gruop2, .button-group3, .button-group4 {
    float: left;
     width: 33.33333%;
     padding: 20px;
     background: #eee;
     box-sizing: border-box;

  }

  .button-group4 {

    margin-right: 0;
  }
</style>