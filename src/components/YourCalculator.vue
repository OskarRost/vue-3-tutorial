
<template>
<ul>
  <li><a class="active" href="#home">Menü</a></li>
  <li><a href="#news">Calculator</a></li>
  <li><a href="#contact">Kontakt</a></li>
</ul>
  <h3>Calculator</h3>

  <div>
    <input type="number" v-model="num1" />
    <input type="number" v-model="num2" />
  </div>
  <div class="button.group">
         <button type="submit" class="button" v-on:click.prevent="add">+</button>
         <button type="submit" class="button" v-on:click.prevent="minus">-</button>
         <button type="submit" class="button" v-on:click.prevent="multiply">*</button>
         <button type="submit" class="button" v-on:click.prevent="geteilt">÷</button>
  </div>
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
    add:
            function () {
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
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  position: -webkit-sticky; /* Safari */
  position: sticky;
  top: 0;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}

.active {
  background-color: #4CAF50;
}
 button {
  display: inline;
	height:40px;
	width:138px;
  margin-top: 10; 
  border: 1px solid;
  cursor: pointer;
  }
</style>