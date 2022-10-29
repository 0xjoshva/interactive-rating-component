<template>
<section>
<div class="container" >
  <div class="form" v-show="monkey === false">
  <img src="../assets/icon-star.svg" alt="">
  <h1>How did we do?</h1>
  <p>Please let us know how we did with your support request. All the feedback is apprecaited to help us improve our offering!</p>
</div>
  <div class="message" v-show="monkey === !false">
    <img src="../assets/illustration-thank-you.svg" alt="">
    <p>You selected {{value}} out of 5</p>
    <h1>Thank you!</h1>
    <p>We appreciate you taking the time to give a rating. If you ever need more support, don't hesitate to get in touch!</p>
  </div>
  <button @click="monkey = false">SUBMIT</button>
</div>
</section>
</template>

<script>

export default {
  data() {
    return {
      monkey: false
  }
}
}
</script>
<style scoped>
section{
  width: 100%;
  height: 100vh;
  background: var(--vdblue);
  display: flex;
  align-items: center;
  justify-content: center;
}
.container{
  width: 25rem;
  height: 25rem;
  border-radius: 16px;
  background:var(--dblue);
}
</style>
