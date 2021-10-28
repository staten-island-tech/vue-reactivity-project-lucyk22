<template>
  <div class="money">



      <div class="shop things"> 


        
        <select class="listy" v-model="selected" multiple>
          <option class="options" v-for="item in items" :key="item" v-bind:value="item">{{ item.itemName }}</option>
        </select>
        
                <span class="dialogue">{{ selected[0].dialogue }} </span>

        <div class="buttons">
          <button v-on:click="purchase" class="buy">buy</button>
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
        {itemCost: 49030
        ,
        itemName: "keygen", dialogue: "TRANSMIT [x] KROMER?"},
        {itemCost: 150,
        itemName:"s. potion", dialogue: "LET'S MAKE A DEAL." },
        {itemCost: 150,
        itemName: "the big one", dialogue: "DON'T FORGET TO [Like and Subscribe] FOR MORE [Hyperlink Blocked]!s"},
        {itemCost: 150,
        itemName: "bshot bowtie", dialogue: "DELICIOUS KROMER"},        
   ],

 }
},


  methods: {
    purchase: function() {
      //walletValue -= {{selected[0].itemcost}};

      /*for (;;) {
        function ohno () {
        alert("WHERE'S YOUR KROMER");
        alert("WAKE UP AND TASTE THE PAIN");
        }
      
      }*/


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

.options {
    overflow: hidden;
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