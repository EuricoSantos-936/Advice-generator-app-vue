<template>
  <div>
    <div class="advicegenerator">
      <p v-if="id" class="adviceid">Advice #{{ id }}</p>
      <p v-if="advice" class="advicequote">"{{ advice }}"</p>
      <p v-else>Loading...</p>
      <div class="divider">
        <img src="../assets/pattern-divider-desktop.svg" alt="divider" class="altdivider">
      </div>
      <div class="dicebox">
        <img src="../assets/icon-dice.svg" alt="dice" @click="fetchAdvice" class="dice">
      </div>
    </div>
    <p class="credits">Coded by <a href="https://portfolio-react-bizhead.vercel.app/">Eurico Santos</a> @2023 Challenge by Frontend Mentor.</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      advice: "",
      id: "",
    };
  },
  methods: {
    fetchAdvice() {
      axios
        .get("https://api.adviceslip.com/advice")
        .then((response) => {
          this.advice = response.data.slip.advice;
          this.id = response.data.slip.id;
        })
        .catch((error) => {
          console.error(error);
        });
    },
  },
  created() {
    // Fetch initial advice when the component is created (on start)
    this.fetchAdvice();
  },
};


</script>