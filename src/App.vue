<template>
  <div class="container">  
  <Header />
  <Expenses @delete-expense ="deleteExpense" :expenses="expenses" />
  </div>
</template>

<script>

import Header from './components/Header'
import Expenses from './components/Expenses'

export default {
  name: 'App',
  components: {
    Header,
    Expenses
  },
  data() {
    return {
      expenses: []
    }
  },
  methods:{
    deleteExpense(id){
      this.expenses = this.expenses.filter((expense) => expense.id !== id)
    }
  },
  created(){
    this.expenses = [
      {
        id:1,
        text: 'Birthday party',
        day: 'August 28 at 3:30pm',
        price: '$100'
      },
      {
        id:2,
        text: 'Buy clothes',
        day: 'August 31 at 1:30pm',
        price: '$600'
      }
    ]
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
