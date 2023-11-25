<template>
    <v-menu>
      <template v-slot:activator="{ props }">
        <v-btn icon="mdi-dots-vertical" v-bind="props" class="logo first">

        </v-btn>
      </template>

      <v-list class="menuList">
        <v-list-item class="item close">
          <v-btn icon="mdi-dots-vertical" class="logo"></v-btn>
        </v-list-item>
        <v-list-item
            v-for="(item, i) in menu"
            :key="i"
            class="item"
        >
          <v-list-item-title>
            {{ item.text }}
          </v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
</template>

<script setup lang="ts">
const menu = [
  {
    href: '',
    text: 'NEWS',
  },
  {
    href: '',
    text: 'SEASONS',
  },
  {
    href: '',
    text: 'CLUB',
  },
  {
    href: '',
    text: 'SHOP',
  },
  {
    href: '',
    text: 'TICKETS',
  },
  {
    href: '',
    text: 'LOGIN',
  }
]
</script>

<style scoped lang="scss">

.item {
  margin-left: 0;
  padding: 5px;
  color: #004996;
  font-weight: bold;
  margin-bottom: 0;
  margin-top: 5px;
  cursor: pointer;
  border: none;
  &:hover {
    background: none;
    border: none;
    box-shadow: none;
  }
}
//
//.menuList {
  //
  //  margin-top: -8px;
  //  margin-bottom: -8px;
  //}

.menuList {
  margin-left: -25px;
  margin-top: -60px;
}

.close {
* {
  margin-bottom: 2px;
  margin-left: 2px;
}
}

.logo {
   background-image: url("../images/realSmall.png");
  margin-top: 0;
  background-color: transparent;
  border: none;
  box-shadow: none;
  margin-left: 10px;
  &:hover {
    background-color: transparent;
    border: none;
    box-shadow: none;
  }
}

.first {
  margin-left: 25px;
}
</style>