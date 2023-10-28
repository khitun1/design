<template>
  <div class="nav">
    <button>NEWS</button>
    <button>SEASON</button>
    <button>CLUB</button>
    <img src="../images/Logo.png"/>
    <button>SHOP</button>
    <button>TICKETS</button>
    <button>LOGIN</button>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
$size: 75px;

.nav {

  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-left: -10px;
img {
  width: $size;
  height: $size;
}
button {
  background: none;
  border: none;
  color: white;
  width: fit-content;
  height: fit-content;
  font-size: 24px;
  font-weight: bold;
  cursor: pointer;
}
}
</style>