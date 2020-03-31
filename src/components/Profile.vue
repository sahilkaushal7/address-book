<template>
  <b-card class="mx-5 px-2">
    <b-row no-gutters>
      <b-col cols="12" sm="4">
        <b-img
          fluid
          style="height: 260px; width: 100%; object-fit: cover"
          rounded
          v-bind:src="activeAddress.image"
          alt="profile"
        />
      </b-col>
      <b-col cols="12" sm="8" class="px-3 py-1">
        <h2>{{activeAddress.name}}</h2>
        <sup>{{activeAddress.status}}</sup>
        <div class="py-2">
          <p style="color: grey; font-size: 12px;">Basic Details :</p>
          <b-row no-gutters align-v="baseline">
            <b-col cols="12" lg="6">
                <b-icon-phone variant="info" font-scale="2" />
                <label style="font-size: 11px;" class="py-1 px-2">
                  <b>Phone Number:</b>
                  <br />
                  {{activeAddress.phoneNumber}}
                </label>
            </b-col>
            <b-col>
              <b-icon-phone variant="info" font-scale="2" />
              <label style="font-size: 11px;" class="py-1 px-2">
                <b>Alternate Number:</b>
                <br />
                {{activeAddress.alternateNumber}}
              </label>
            </b-col>
          </b-row>
          <p class="pt-3">
            <b-icon-calendar variant="info" font-scale="2" />
            <label style="font-size: 11px;" class="px-2">
              <b>Date of birth:</b>
              <br />
              {{activeAddress.dob}}
            </label>
          </p>
        </div>
      </b-col>
    </b-row>
  </b-card>
</template>

<script>
export default {
  name: "Profile",
  props: ["activeAddress"]
};
</script>