<template>
    <div>
      <p>Time left: {{ timeLeft }} seconds</p>
    </div>
  </template>
  
  <script>
  export default {
    name: "Practice",
  
    data() {
      return {
        timeLeft: 10,
        timer: null
      };
    },
  
    // Lifecycle hook - 1
    mounted() {
      // Start the timer when the component is mounted
      console.log("Component mounted: Starting countdown timer.");
      this.startTimer();
    },
  
    // Lifecycle hook - 2
    beforeUnmount() {
      // Clean up the timer before the component is removed from the DOM
      console.log("Component about to be unmounted: Stopping timer.");
      clearInterval(this.timer);
    },
  
    methods: {
      startTimer() {
        this.timer = setInterval(() => {
          if (this.timeLeft > 0) {
            this.timeLeft--;
          } else {
            clearInterval(this.timer);
            console.log("Countdown finished!");
          }
        }, 1000);
      }
    }
  };
  </script>
  
  <style scoped>
  p {
    font-size: 20px;
    color: #333;
  }
  </style>
  