<template>
  <div class="fix">
    <nav class="nav">
      <ul>
        <li>
          <img src="../images/Logo.png" alt="logo"/>
        </li>
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
          <a>SHOP</a>
        </li>
        <li>
          <a>TICKETS</a>
        </li>
        <li>
          <a>LOGIN</a>
        </li>
        <li>
          <a>
            <img src="../images/Lang.png" alt="language"/>
            EN
          </a>
        </li>
      </ul>
      <div class="menu">
        <DropDown/>
      </div>
    </nav>
  </div>
</template>

<script setup lang="ts">

  import DropDown from "@/components/DropDown.vue";


</script>

<style scoped lang="scss">
$size: 75px;

.nav {
  background: #EAEAEA;
  display: flex;
  width: 100%;
  height: 60px;
  padding-top: 5px;
  align-items: center;
  font-family: Arial;
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
  img {
    width: $size;
    height: $size;
  }
  a {
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

.menu {
  display: none;
}



@media screen and (max-width: 400px) {
  .menu {
    display: block;
  }

  .nav {
    ul {
      display: none;
    }
  }
}

</style>