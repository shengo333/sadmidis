<template>
  <div id="footer">
      <h2>Now you now how much goverment is taking from our work</h2>
  </div>

  <div id="button">
    <button @click="storeData">Store data</button>
    <button @click="clearData">Clear data</button>
  </div>

</template>

<script>
export default {
    name: 'Footer',
    methods:{
      storeData(){

      },
      clearData(){
        
      }
    }
}
</script>

<style scoped>

#footer{
  text-align: center;
  padding: 15px;
  border-top: solid gray;
  border-radius: 5px;
}
button{
  display: inline-block;
  padding: 10px 5px 10px 5px;
  max-width: 170px;
  text-align: center;
  background: rgb(117, 211, 195);
  margin: 15px auto auto auto;
  border-radius: 5px;
  font-size: 20px;
  margin: 10px;
}

#button{
  display: flex;
  justify-content: center;
}

</style>