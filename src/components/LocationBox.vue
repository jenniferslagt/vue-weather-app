<template>
    <div class="location-box">
        <div class="location">{{ weather.name }}, {{ weather.sys.country }}</div>
        <div class="date">{{ dateBuilder() }}</div>
    </div>
</template>

<script>
export default {
    name: "LocationBox",
     props: {
        weather: Object
    },
    methods: {
    dateBuilder() {
      let d = new Date();
      let months = ["January", "Febraury", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
      let days = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];

      let day = days[d.getDay()];
      let date = d.getDate();
      let month = months[d.getMonth()];
      let year = d.getFullYear();

      return `${day} ${date} ${month} ${year}`
    }
    }
}
</script>

<style scoped>
.location-box .location {
    color: #fff;
    font-size: 32px;
    font-weight: 500;
    text-align: center;
    text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
  }

  .location-box .date {
    color: #fff;
    font-size: 20px;
    font-weight: 300;
    font-style: italic;
    text-align: center;
  }
</style>