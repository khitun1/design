<template>
  <div class="fix">
    <div class="nav">
      <img src="../images/Logo.png"/>
      <button>NEWS</button>
      <button>SEASON</button>
      <button>CLUB</button>
      <button>SHOP</button>
      <button>TICKETS</button>
      <button>LOGIN</button>
      <button>
        <img src="../images/Lang.png"/>
        EN
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
$size: 75px;

.nav {
  background: #EAEAEA;
  margin-top: -10px;
  display: flex;
  width: 100%;
  padding-top: 5px;
  height: fit-content;
  justify-content: space-between;
  align-items: center;
  img {
    width: $size;
    height: $size;
  }
  button {
    background: none;
    border: none;
    color: #004996;
    width: fit-content;
    height: fit-content;
    font-size: 24px;
    font-weight: bold;
    cursor: pointer;

    img {
      width: 20px;
      height: 20px;
    }
  }
}

.fix {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

</style>