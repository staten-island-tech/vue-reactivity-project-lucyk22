<template>
  <div class="main">
    <h1>HI   EVERY  !</h1>
    <div class="spamton">
      <img src="../assets/spamton.png" alt="">
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


