<template>
  <div class="footer">
    <div class="connection">
      <div class="nets">
        <h3>FOLLOW US</h3>
        <div class="icons">
          <img src="../images/vk.png" alt="vk"/>
          <img src="../images/youTube.png" alt="youTube"/>
          <img src="../images/snapchat.png" alt="snapchat"/>
        </div>
      </div>
      <div class="apps">
        <h3>REAL MADRID APP</h3>
        <div class="icons">
          <img src="../images/appStore.png" alt="appStore"/>
          <img src="../images/googlePlay.png" alt="googlePlay"/>
        </div>
      </div>
    </div>
    <div class="rights">
      Real Madrid © 2023 All rights reserved
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">

.footer {
  background-color: #004996;
  width: 100%;
  margin-bottom: -10px;
  height: fit-content;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  margin-top: 50px;
  font-family: Arial;
}

.connection {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
  width: 100%;
}

.nets, .apps {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  color: white;
  font-weight: normal;
  margin-top: 0;
  width: 15%;
  height: fit-content;
}

  .icons {
    display: flex;
    flex-direction: row;
    width: 80%;
    justify-content: space-between;
    img {
      cursor: pointer;
    }
  }

.nets {
  margin-top: -5px;
}

h3 {
  font-size: 20px;
  height: fit-content;
}

.rights {
  margin-bottom: 10px;
}
</style>