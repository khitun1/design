<template>
  <div class="fix">
    <nav class="nav">
      <ul>
        <li>
          <a>NEWS</a>
        </li>
        <li>
          <a>SEASON</a>
        </li>
        <li>
          <a>CLUB</a>
        </li>
        <li>
          <img src="../images/Logo.png" alt="logo"/>
        </li>
        <li>
          <a>SHOP</a>
        </li>
        <li>
          <a>TICKETS</a>
        </li>
        <li>
          <a>LOGIN</a>
        </li>
      </ul>

    </nav>
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
  font-family: Arial;
  img {
    width: $size;
    height: $size;
  }
  ul {
    display: flex;
    width: 100%;
    height: fit-content;
    justify-content: space-between;
    align-items: center;

    margin: 0;
    padding-right: 10px;
    li {
      list-style-type: none;
      padding: 0;
    }
  }
  a {
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

.fix {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
</style>