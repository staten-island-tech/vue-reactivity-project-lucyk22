<template>
  <div class="money">
    <div class="shop kromer"> 
        <p>kromr</p>
         </div>
      <div class="shop things"> 
        
        <select class="listy" v-model="items" multiple>
          <option v-for="item in items" :key="item" v-bind:value="item.itemId">{{ item.itemName }}</option>
        </select>
         </div>
      
            
      
  </div>
</template>

<script>
 export default {
  name: 'Shop',
   data() {
 return {
   items: [
        {itemId: 1,
        itemName: "hello"},
        {itemId: 2,
        itemName:"crying and crumbling" },
        {itemId: 3,
        itemName: "groaning and grumbling"},
        {itemId: 4,
        itemName: "AAAAAAAAAAAAAAAAAAAAAAAA"},
        
   ]


 }
}
}
</script>

<style>

.money {
  margin: 2rem;
}

.shop {
  background: black;
  color: white;
  margin: 1rem auto;
  padding: 2rem;
  font-size: 1.5rem;
  text-transform:uppercase;
  border-style: solid;
  border-color: white;
  
}

.kromer {
  width: 70%;
}

.listy {
  background-color: black;
  color: white;
  border:none;
  font-size: 1.5rem;
  text-transform:uppercase;
}

</style>