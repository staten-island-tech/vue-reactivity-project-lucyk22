<template>
  <div class="money">
    <div class="shop kromer"> 
        <button class="buy catalog">shop</button>
        <button class="buy talk">talk</button>
        <button class="buy bye">bye</button>
         </div>
      <div class="shop things"> 
        
        <select class="listy" v-model="selected" multiple>
          <option class="options" v-for="item in items" :key="item" v-bind:value="item.dialogue">{{ item.itemName }}</option>
        </select>
        <span>{{ selected }} </span>
         </div>
      
            
      
  </div>
</template>

<script>
 export default {
  name: 'Shop',
   data() {
 return {
   selected: '',
   items: [
        {itemId: 1,
        itemName: "keygen", dialogue: "TRANSMIT [x] KROMER?"},
        {itemId: 2,
        itemName:"s. potion", dialogue: "LET'S MAKE A DEAL." },
        {itemId: 3,
        itemName: "the big one", dialogue: "DON'T FORGET TO [Like and Subscribe] FOR MORE [Hyperlink Blocked]!s"},
        {itemId: 4,
        itemName: "bshot bowtie", dialogue: "DELICIOUS KROMER"},
        
   ]


 }
}
}
</script>

<style>

.buy {
  background: black;
  color:white;
  border:white;
  font-size: 1rem;
  border:solid;
  padding: .5rem;
  margin:.1rem;
}

.buy:hover {
  color: yellow;
}



.money {
  margin: 2rem;

}

.shop {
  background: black;
  color: white;
  margin: 1rem auto;
  padding: 1rem;
  font-size: 1.5rem;
  text-transform:uppercase;
  border-style: solid;
  border-color: white;
  
}

.kromer {
  width: 70%;
}

.options {
  margin-top: 1rem;

}

.options:hover {
  color:yellow;
}

.listy {
  background-color: black;
  color: white;
  border:none;
  font-size: 1.5rem;
  text-transform:uppercase;
}

</style>