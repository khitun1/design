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

    @media screen and (max-width: 400px) {
      justify-content: space-between;
      margin-right: 10px;
      margin-bottom: 10px;
    }
  }

  .nets, .apps {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    color: white;
    font-weight: normal;
    margin-top: 0;
    width: 15%;
    @media screen and (max-width: 400px) {
      h3 {
        margin-bottom: 20px;
        margin-top: 10px;
      }
      width: fit-content;
    }
    height: fit-content;
  }

    .icons {
      display: flex;
      flex-direction: row;
      width: 80%;
      justify-content: space-between;
      img {
        cursor: pointer;
        @media screen and (max-width: 400px) {
          width: 20%;
          margin-top: -10px;
        }
      }
    }

  .nets {
    margin-top: -5px;
    //@media screen and (max-width: 400px) {
    //  margin-left: -50px;
    //  margin-right: 50px;
    //}
  }

  h3 {
    font-size: 20px;
    height: fit-content;

    @media screen and (max-width: 400px) {
      font-size: 16px;
    }
  }

  .rights {
    margin-bottom: 10px;
    @media screen and (max-width: 400px){
      font-size: 14px;
      margin-top: 10px;
    }

  }

  .apps {
    @media screen and (max-width: 400px){
      margin-top: -5px;
      .icons {
        justify-content: space-around;
      }
    }
  }
</style>