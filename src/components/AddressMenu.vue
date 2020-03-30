<template>
  <div class="address-menu">
    <h3>Address Book</h3>
    <div v-bind:key="address.id" v-for="address in addresses" class="address-menu__item">
      <img class="address-menu__item-img" v-bind:src="address.image" />
      <div>
        <b>{{address.name}}</b>
        <h6>{{address.status}}</h6>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AddressMenu",
  props: ["addresses"]
};
</script>

<style scoped>
::-webkit-scrollbar {
  width: 5px;
}

::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px #ebebec; 
  border-radius: 10px;
}

::-webkit-scrollbar-thumb {
  background: #659bc3; 
  border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #006ebf; 
}

.address-menu {
  background-color: #252529;
  width: 20%;
  height: 100vh;
  overflow-y: scroll;
  color: #f6fafd;
}

.address-menu h3 {
  text-align: center;
  padding: 10px;
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

.address-menu__item-img {
  width: 50px;
  height: 50px;
  border-radius: 25px;
  margin-right: 10px;
}
</style>

