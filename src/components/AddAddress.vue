<template>
  <b-card title="Add a new address" class="m-5 px-2">
    <b-form @submit.prevent="$emit('submit-address', form)">
      <b-form-group id="input-group-1" label="Name:" label-for="input-1">
        <b-form-input 
          id="input-1" 
          v-model="form.name" 
          required 
          placeholder="Enter name"
        ></b-form-input>
      </b-form-group>
      <b-form-group id="input-group-2" label="Address:" label-for="input-2">
        <b-form-input 
          id="input-2" 
          v-model="form.address"
          required 
          placeholder="Enter Address"
        ></b-form-input>
      </b-form-group>
      <b-form-group id="input-group-3" label="Phone Number:" label-for="input-3">
        <b-form-input
          id="input-3"
          v-model="form.phoneNumber"
          required
          placeholder="Enter Phone Number"
        ></b-form-input>
      </b-form-group>
      <b-form-group id="input-group-4" label="Alternate Number:" label-for="input-4">
        <b-form-input
          id="input-4"
          v-model="form.alternateNumber"
          required
          placeholder="Enter Alternate Number"
        ></b-form-input>
      </b-form-group>
      <b-form-group id="input-group-5" label="DOB:" label-for="input-5">
        <b-form-input 
          id="input-5" 
          v-model="form.dob" 
          required 
          placeholder="Enter Date of Birth"
        ></b-form-input>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
  </b-card>
</template>

<script>
export default {
  name: "AddAddress",
  data() {
    return {
      form: {
        name: "",
        address: "",
        phoneNumber: "",
        alternateNumber: "",
        dob: ""
      }
    };
  }
};
</script>