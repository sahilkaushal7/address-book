<template>
  <div class="address-menu">
    <b-row align-v="center" no-gutters>
      <b-col cols="10">
        <h3>Address Book</h3>
      </b-col>
      <b-col cols="2">
        <b-icon-person-plus
          @click="$emit('add-address')"
          font-scale="2"
          class="border rounded p-2"
        />
      </b-col>
    </b-row>
    <div v-bind:key="address.id" v-for="address in addresses">
      <AddressMenuItem
        v-bind:address="address"
        v-on:change-menuitem="$emit('change-menuitem', address.id)"
      />
    </div>
  </div>
</template>

<script>
import AddressMenuItem from "./AddressMenuItem";

export default {
  name: "AddressMenu",
  props: ["addresses", "activeAddress"],
  components: {
    AddressMenuItem
  }
};
</script>

<style scoped>
::-webkit-scrollbar {
  width: 5px;
}

::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px #ebebec;
  border-radius: 5px;
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
  height: 100vh;
  overflow-y: scroll;
  color: #f6fafd;
}

.address-menu h3 {
  text-align: center;
  padding: 10px;
}

@media only screen and (max-width: 767px) {
  .address-menu {
    height: 200px;
  }
}
</style>

