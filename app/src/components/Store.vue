<template>
  <div class="money">



      <div class="shop things"> 


        
        <select class="listy" v-model="selected" multiple>
          <option class="options" v-for="item in items" :key="item.itemID" v-bind:value="item">{{ item.itemName }}</option>
        </select>
        
                <span class="dialogue">{{ selected[0].dialogue }} </span>

        <div class="buttons">
          <button v-on:click="purchase(); debt();" class="buy">buy</button>
          <span class="cost"> -D${{selected[0].itemCost}}</span>
        </div>

      </div>

      <div class="shop kromer"> 
        <span class="wallet">D${{ walletValue }}</span>
        
      </div>
            
      
  </div>
  
</template>

<script>
 export default {
  name: 'Shop',
   data() {
 return {
   selected: [
     {itemCost: "0",
     dialogue: "",}
   ],

   walletValue: 5000,
   items: [
        {itemID: 1,
        itemCost: Math.floor(Math.random() * 49030)
        ,
        itemName: "keygen", dialogue: "TRANSMIT [x] KROMER?"},
        {itemID: 2, itemCost: Math.floor(Math.random() * 150),
        itemName:"s. potion", dialogue: "LET'S MAKE A DEAL." },
        {iitemID: 3, itemCost: Math.floor(Math.random() * 150),
        itemName: "the big one", dialogue: "DON'T FORGET TO [Like and Subscribe] FOR MORE [Hyperlink Blocked]!s"},
        {itemID: 4, itemCost: Math.floor(Math.random() * 150),
        itemName: "bshot bowtie", dialogue: "DELICIOUS KROMER"},        
   ],

 }
},


  methods: {
    purchase: function() {
      this.walletValue -= this.selected[0].itemCost;
    },
    debt: function() {
      //walletValue -= {{selected[0].itemcost}};
      while (this.walletValue < 0) {
        alert("WHERE'S YOUR KROMER");
        alert("WAKE UP AND TASTE THE PAIN");
        alert("You have been gifted 5000 kromer by [[BIG SIMP]]");
        this.walletValue += 5000;
      }
  


    }
  },
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
  margin:.5rem;

}

.buy:hover {
  color: yellow;
}



.money {
  margin: 2rem;
  width: 40%;
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
  display: flex;
  flex-direction: column;


}

.dialogue {
  margin: 1rem;
  width: 90%;
}

.kromer {
  width: 70%;
}

.options {
  margin: 1rem;
  border-style: solid;
  border-color: white;
  width: 80%;
      overflow: hidden;

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