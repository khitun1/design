<template>
  <div class="trophy">
    <slot>

    </slot>
    <div class="amount">
      {{amount}}
    </div>
    <div class="des">
      {{description}}
    </div>
  </div>
</template>

<script setup lang="ts">

const {amount, description} = defineProps({
  amount: String,
  description: String,
})
</script>

<style scoped lang="scss">

  .trophy {
    width: 25%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin-right: 10px;

    @media screen and (max-width: 400px) {

      .amount {
        font-size: 20px;
      }

      .des {
        font-size: 12px;
      }
    }

    * {
      margin-top: 5px;
    }
  }

  .des {
    text-align: center;
    color: #818181;
    font-size: 14px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial;
  }

  .amount {
    color: #004996;
    font-size: 30px;
    font-family: Arial;


  }
</style>