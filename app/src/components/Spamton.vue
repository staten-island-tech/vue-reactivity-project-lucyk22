<template>
  <div class="main">
    <h1>HI   EVERY  !</h1>
    <div class="spamton">
      <img src="../assets/spamton.png" alt="" class=spammy>
    </div>
    <div class="dialogue-box" v-on:click="advText">
      <p id="talkText" class="dialogue-text"> {{talkText[Math.floor(Math.random() * 4)].text}}</p>
    </div>
  </div>
</template>

<script>
 export default {
  name: 'Spamton',
  props: {
    dialogue: String
  },
  data() {
 return {
   talkText: [
     {text: "what?! you have [[no kromer]]? then just give your [[heartshapedobject]] instead!"},
     {text:"it's everyone's favorite [[numberonesalesman1997]], Spamton G. Spamton!!!!!"},
     {text:"I've got a [[specil deal]] for you!"},
     {text:"why be the [[little sponge]] who hates its [[$4.99]] life"},
   ],

 }
},

methods: {
  advText: function () {
    const tText = document.getElementById("talkText");
    const talkText = [
     {text: "what?! you have [[no kromer]]? then just give your [[heartshapedobject]] instead!"},
     {text:"it's everyone's favorite [[numberonesalesman1997]], Spamton G. Spamton!!!!!"},
     {text:"I've got a [[specil deal]] for you!"},
     {text:"why be the [[little sponge]] who hates its [[$4.99]] life"} ]

    tText.innerText = talkText[Math.floor(Math.random() * 4)].text;

  }
},

 }

</script>

<style>
.main {
  display:flex;
  flex-direction: column;
  align-items: center;
  width: 50%;
}

.spammy {
  width: 70%
}
.dialogue-box {
  background: black;
  color: white;
  margin: 1rem auto;
  padding: 0rem 2rem 0rem 2rem;
  font-size: 1.5rem;
  text-transform:uppercase;
  border-style: solid;
  border-color: white;
  width: 90%;
  height: 10rem;
  
}

</style>
