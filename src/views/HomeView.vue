<template>
  <section>
    <div class="container">
      <div class="form" v-show="monkey === false">
        <img src="../assets/icon-star.svg" alt="" class="star" />
        <h1>How did we do?</h1>
        <p>
          Please let us know how we did with your support request. All the
          feedback is apprecaited to help us improve our offering!
        </p>
        <div class="radio-buttons">
          <button
            @click="value = 1"
            class="radio-btn"
            :class="{ focus: value === 1 }"
          >
            1
          </button>
          <button
            @click="value = 2"
            class="radio-btn"
            :class="{ focus: value === 2 }"
          >
            2
          </button>
          <button
            @click="value = 3"
            class="radio-btn"
            :class="{ focus: value === 3 }"
          >
            3
          </button>
          <button
            @click="value = 4"
            class="radio-btn"
            :class="{ focus: value === 4 }"
          >
            4
          </button>
          <button
            @click="value = 5"
            class="radio-btn"
            :class="{ focus: value === 5 }"
          >
            5
          </button>
        </div>
      </div>
      <div class="message" v-show="monkey === true">
        <img src="../assets/illustration-thank-you.svg" alt="" />
        <p id="score">You selected {{ value }} out of 5</p>
        <h1>Thank you!</h1>
        <p id="thanks">
          We appreciate you taking the time to give a rating. If you ever need
          more support, don't hesitate to get in touch!
        </p>
      </div>
      <button class="submit" @click="monkey = true" :class="{ hide: monkey }">
        SUBMIT
      </button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      monkey: false,
      value: 0,
    };
  },

};
</script>
<style scoped>
section {
  width: 100%;
  height: 100vh;
  background: var(--vdblue);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: "Overpass", sans-serif;
}
.container {
  width: 25rem;
  height: 25rem;
  border-radius: 26px;
  background: var(--dblue);
  padding: 2rem;
}

.star {
  background: rgba(128, 128, 128, 0.11);
  padding: 1rem;
  border-radius: 50%;
  margin-bottom: 1.5rem;
}
h1 {
  color: var(--white);
  font-size: 1.8rem;
  font-weight: 700;
}
p {
  color: var(--lgrey);
}
.submit {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 26px;
  background: var(--orange);
  color: var(--white);
  letter-spacing: 2px;
  border: none;
  outline: none;
  line-height: 40px;
  transition: .2s ease-in-out all;
}
.submit:hover {
  background: var(--white);
  color: var(--orange);
}
.message {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  animation: fade linear 1s;
}
@keyframes fade {
  0%{
    opacity: 0;
  }
  100%{
    opacity: 1;
  }
}
#score {
  color: var(--orange);
  background: rgba(128, 128, 128, 0.11);
  font-size: 1rem;
  font-weight: 100;
  padding: 0.2rem 0.8rem;
  border-radius: 26px;
  margin-top: 1.5rem;
  margin-bottom: 2rem;
}
#thanks {
  text-align: center;
  padding-top: 0.2rem;
}
.radio-buttons {
  display: flex;
  width: 100%;
  justify-content: space-between;
  margin-top: 2rem;
  margin-bottom: 2.5rem;
}
.radio-btn {
  padding: 1rem 1.4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  background: rgba(128, 128, 128, 0.11);
  color: var(--lgrey);
  line-height: normal;
  border: none;
  outline: none;
 transition: .2s cubic-bezier(0.45, 0.05, 0.55, 0.95) all;
}
.focus {
  background: var(--orange) !important;
  color: var(--white) !important;
  scale: 1.1;
}
.radio-btn:hover {
  background: var(--mgrey);
  color: var(--white);
}
.hide {
  display: none;
}
.form {
}
</style>