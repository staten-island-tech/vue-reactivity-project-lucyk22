<template>
  <div class="main">
    <h1>HI   EVERY  !</h1>
    <div class="spamton">
      <img src="../assets/spamton.png" alt="" class=spammy>
    </div>
    <div class="dialogue-box">
      <p class="dialogue-text"> {{dialogue}}</p>
    </div>
    <div class="  "></div>
  </div>
</template>

<script>
 export default {
  name: 'Spamton',
  props: {
    dialogue: String
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
  width: 70%;
  margin: 1rem auto;
  padding: 2rem;
  font-size: 1.5rem;
  text-transform:uppercase;
  border-style: solid;
  border-color: white;
  
}

</style>
