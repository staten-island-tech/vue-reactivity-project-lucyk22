<template>
  <div class="main">
    <h1>HI   EVERY  !</h1>
    <div class="spamton">
      <img src="../assets/spamton.png" alt="" class=spammy>
    </div>
    <div class="dialogue-box">
      <p class="dialogue-text"> {{intro}}</p>
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
   noKromer: "what?! you have [[no kromer]]? then just give your [[heartshapedobject]] instead!",
   intro: "it's everyone's favorite [[numberonesalesman1997]], Spamton G. Spamton!!!!!",
   deal: "I've got a [[specil deal]] for you!",
   talk: "why be the [[little sponge]] who hates its [[$4.99]] life",

 }
}

 }

</script>

<style>
.main {
  display:flex;
  flex-direction: column;
  align-items: center;
}

.spammy {
  width: 70%
}
.dialogue-box {
  background: black;
  color: white;
  margin: 1rem auto;
  padding: 2rem;
  font-size: 1.5rem;
  text-transform:uppercase;
  border-style: solid;
  border-color: white;
  
}

</style>
