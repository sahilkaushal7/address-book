<template>
  <div class="address-menu__item" @click="$emit('change-menuitem', address.id)">
    <img class="address-menu__item-img" v-bind:src="address.image" />
    <div>
      <b>{{address.name}}</b>
      <h6>{{address.status}}</h6>
    </div>
  </div>
</template>

<script>
export default {
  name: "AddressMenuItem",
  props: ["address"]
};
</script>

<style scoped>
  .address-menu__item-img {
    width: 50px;
    height: 50px;
    border-radius: 25px;
    margin-right: 10px;
  }

  .address-menu__item {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 8px;
    border-top: 1px solid #ebebec;
    word-break: break-all;
  }

  .address-menu__item:hover {
    background: #ebebec;
    color: #252529;
    cursor: pointer;
  }
</style>