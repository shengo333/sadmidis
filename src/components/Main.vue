<template>

    <div class="card">
      <input type="number" placeholder="Please enter your salary" v-model="amount">
      <button @click="updateTaxes">Get the information</button>
    </div>
  
  <h2>Salary  is: {{amount}}</h2>
  <h2>Income tax is: {{incomeTax}}</h2>
  <h2>Education budget is: {{educationBudget}}</h2>
  <h2>Military service budget is: {{militaryBudget}}</h2>
  <h2>Security service budget is: {{securityBudget}}</h2>
  <h2>healthcare service budget is: {{healscareBudget}}</h2>
  <h2>Government  eats: {{governmentBudget}}</h2>


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
      governmentBudget () {
        if(this.amount) {
          return this.educationBudget + this.militaryBudget + this.securityBudget + this.healscareBudget
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
  padding-top: 20px;

}

h2{
  padding: 5px 0 5px 0;
}

input{
  display: inline-block;
  padding: 15px 0 15px 0;
  max-width: 170px;
  text-align: center;
  justify-content: center;
  background: whitesmoke;
  margin: auto;
  border-radius: 5px;
}

button{
  display: inline-block;
  padding: 10px 0 10px 0;
  max-width: 170px;
  text-align: center;
  background: rgb(117, 211, 195);
  margin: 15px auto auto auto;
  border-radius: 5px;
  font-size: 20px;
}


</style>