<template>
       <div class="search-box">
          <input type="text" class="search-bar" placeholder="Search locations.."
       @keypress.enter="$emit('search', $event.target.value)"/>
      </div>
</template>

<script>
export default {
    name: "SearchBox",
}
</script>

<style scoped>
.search-box {
    width: 100%;
    margin-bottom: 30px;
  }

.search-bar {
    display: block;
    width: 100%;
    padding: 15px;
    color: black;
    font-size: 20px;
    appearance: none;
    border: none;
    outline: none;
    box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
    background: none;
    background-color: rgba(255, 255, 255, 0.671);
    border-radius: 0px 16px 0px 16px;
    transition: 0.4s;
  }

 .search-bar:focus {
    background-color: rgb(255, 255, 255);
    box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
    border-radius: 0px 16px 0px 16px;
  }
</style>