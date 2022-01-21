<template>
  <h2>this is main part</h2>

    <div class="card">
      <input type="number" placeholder="0" v-model="amount">
      <button @click="updateTaxes">click me to get information</button>
    </div>
  
  <h2>Salary  is: {{amount}}</h2>
  <h2>income tax is: {{incomeTax}}</h2>
  <h2> Education budget is: {{educationBudget}}</h2>
  <h2>Military service budget is: {{militaryBudget}}</h2>
  <h2>Security service budget is: {{securityBudget}}</h2>
  <h2>healthcare service budget is: {{healscareBudget}}</h2>
  <h2>Irakli eats: {{irakliBudget}}</h2>


</template>

<script>
export default {
    name: 'Main',
    data(){
      return{
        amount: '',
        incomeTax: '',
        militaryBudget: '',
        securityBudget: '',
        healscareBudget: '',
        educationBudget: '',
      }
    },
    methods:{
      updateTaxes(){
        this.incomeTax = (this.amount * 0.2)
        this.educationBudget = (this.incomeTax * 0.2)
        this.militaryBudget = (this.incomeTax * 0.1)
        this.securityBudget = (this.incomeTax * 0.2)
        this.healscareBudget = (this.incomeTax * 0.5)
        
      }
    },
    computed: {
      irakliBudget () {
        if(this.amount) {
          return this.amount * 2
        } else {
          return 0
        }
      }
    }
} 
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  max-width: 300px;
  margin: auto;

}

input{
  display: inline-block;
  padding: 3px;
  text-align: center;
  background: whitesmoke;
  margin: 5px;
  border-radius: 5px;
}

button{
  display: inline-block;
  padding: 15px;
  text-align: center;
  background: rgb(96, 192, 52);
  margin: 5px;
  border-radius: 5px;
  font-family: sans-serif;
  font-size: 20px;
}


</style>