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

<style scoped>

.trophy {
  width: 239px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-right: 10px;
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
}

.amount {
  color: #004996;
  font-size: 30px;
}
</style>