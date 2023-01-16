<template>
  <div class="container">
    <div class="overlay">
      <img src="../assets/images/image-jeremy.png" alt="portrait" />
      <p>Report for</p>
      <h1>Jermemy Robson</h1>
    </div>
    <div class="menu">
      <button @click="(timeframe = 'daily'), (description = 'Yesterday')">
        Daily
      </button>
      <button @click="(timeframe = 'weekly'), (description = 'Last Week')">
        Weekly
      </button>
      <button @click="(timeframe = 'monthly'), (description = 'Last Month')">
        Monthly
      </button>
    </div>
    <div class="categories" v-for="item in items" :key="item.title">
      <h3>{{ item.title }}</h3>
      <h2>{{ item.timeframes[timeframe].current }}hrs</h2>
      <p>{{ description + " " + item.timeframes[timeframe].previous }}hrs</p>
    </div>
  </div>
</template>

<script>
import data from "../../data.json";
export default {
  name: "TimeTrackingDashboard",
  data() {
    return {
      items: data,
      timeframe: "weekly",
      description: "Last Week",
    };
  },
};
</script>

<style scoped></style>
