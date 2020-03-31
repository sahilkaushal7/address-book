<template>
  <div>
    <b-row no-gutters>
      <b-col md="4">
        <AddressMenu
          v-bind:addresses="addresses"
          v-on:change-menuitem="changeMenuItem"
          v-on:add-address="addAddress"
          v-bind:activeAddress="activeAddress"
        />
      </b-col>
      <b-col md="8">
        <Profile v-if="Boolean(activeAddress)" v-bind:activeAddress="activeAddress" />
        <AddAddress v-else v-on:submit-address="submitAddress" />
      </b-col>
    </b-row>
  </div>
</template>

<script>
import AddressMenu from "./components/AddressMenu";
import Profile from "./components/Profile";
import AddAddress from "./components/AddAddress";
import "bootstrap/dist/css/bootstrap.css";
import "bootstrap-vue/dist/bootstrap-vue.css";

export default {
  name: "App",
  components: {
    AddressMenu,
    Profile,
    AddAddress
  },
  data() {
    return {
      activeAddress: null,
      addresses: [
        {
          name: "Hadassah",
          address: "Ap #949-9370 Etiam Rd.",
          phoneNumber: "16440529 7294",
          alternateNumber: "09281076899",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 1,
          dob: "04/03/68"
        },
        {
          name: "Ima",
          address: "597-3147 Eget Avenue",
          phoneNumber: "16930721 6193",
          alternateNumber: "12576040699",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 2,
          dob: "12/29/88"
        },
        {
          name: "Tad",
          address: "3210 Aliquam Rd.",
          phoneNumber: "16050904 6447",
          alternateNumber: "96868893599",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 3,
          dob: "10/13/60"
        },
        {
          name: "Odysseus",
          address: "4621 Parturient Rd.",
          phoneNumber: "16740221 5508",
          alternateNumber: "47458816099",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 4,
          dob: "08/14/40"
        },
        {
          name: "Zephania",
          address: "4027 Risus Rd.",
          phoneNumber: "16900902 3707",
          alternateNumber: "22441966299",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 5,
          dob: "01/20/73"
        },
        {
          name: "Barclay",
          address: "795-6380 Augue Street",
          phoneNumber: "16230129 6915",
          alternateNumber: "06302614899",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 6,
          dob: "12/30/93"
        },
        {
          name: "Bree",
          address: "P.O. Box 145, 4422 Feugiat Road",
          phoneNumber: "16401114 2322",
          alternateNumber: "84360380599",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 7,
          dob: "07/07/74"
        },
        {
          name: "Hop",
          address: "Ap #294-2280 Integer Rd.",
          phoneNumber: "16211114 9536",
          alternateNumber: "62614795999",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 8,
          dob: "03/12/93"
        },
        {
          name: "Lyle",
          address: "P.O. Box 275, 9744 Est Street",
          phoneNumber: "16490927 5325",
          alternateNumber: "21881069499",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 9,
          dob: "04/12/45"
        },
        {
          name: "Ulla",
          address: "625-342 Natoque Av.",
          phoneNumber: "16120103 6140",
          alternateNumber: "75781683699",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 110,
          dob: "10/03/92"
        },
        {
          name: "Barry",
          address: "423-4954 Suspendisse Street",
          phoneNumber: "16580612 8400",
          alternateNumber: "33810425099",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 121,
          dob: "11/28/53"
        },
        {
          name: "Chancellor",
          address: "359-6400 Dictum Av.",
          phoneNumber: "16640921 6881",
          alternateNumber: "68281866499",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 12,
          dob: "08/07/58"
        },
        {
          name: "Blythe",
          address: "4149 Nec Street",
          phoneNumber: "16890721 7676",
          alternateNumber: "06392981399",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 13,
          dob: "11/13/53"
        },
        {
          name: "Maggie",
          address: "521-9609 Mi Ave",
          phoneNumber: "16351108 6344",
          alternateNumber: "35969681199",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 14,
          dob: "04/11/78"
        },
        {
          name: "Martin",
          address: "4471 Condimentum Avenue",
          phoneNumber: "16540122 0545",
          alternateNumber: "93517245599",
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available",
          id: 15,
          dob: "11/13/85"
        }
      ]
    };
  },
  methods: {
    changeMenuItem(id) {
      const address = this.addresses.find(address => address.id === id);
      this.activeAddress = address;
    },
    addAddress() {
      this.activeAddress = null;
    },
    submitAddress(form) {
      const newAddress = Object.assign(
        {},
        {
          id: this.addresses.length + 1,
          image:
            "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg",
          status: "Available"
        },
        form
      );
      this.addresses.unshift(newAddress);
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
  background-color: #ebebec;
}
</style>
