<template>
  <div>
    <AddressMenu v-bind:addresses="addresses" />
  </div>
</template>

<script>
import AddressMenu from "./components/AddressMenu";

export default {
  name: "App",
  components: {
    AddressMenu
  },
  data() {
    return {
      addresses: [
        {
          name: "Dennis",
          address: "8965 Ac St.",
          phoneNumber: "16940316 4479",
          alternateNumber: "72726661399",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "11/30/76"
        },
        {
          name: "Hadassah",
          address: "Ap #949-9370 Etiam Rd.",
          phoneNumber: "16440529 7294",
          alternateNumber: "09281076899",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "04/03/68"
        },
        {
          name: "Ima",
          address: "597-3147 Eget Avenue",
          phoneNumber: "16930721 6193",
          alternateNumber: "12576040699",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "12/29/88"
        },
        {
          name: "Tad",
          address: "3210 Aliquam Rd.",
          phoneNumber: "16050904 6447",
          alternateNumber: "96868893599",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "10/13/60"
        },
        {
          name: "Odysseus",
          address: "4621 Parturient Rd.",
          phoneNumber: "16740221 5508",
          alternateNumber: "47458816099",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "08/14/40"
        },
        {
          name: "Zephania",
          address: "4027 Risus Rd.",
          phoneNumber: "16900902 3707",
          alternateNumber: "22441966299",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "01/20/73"
        },
        {
          name: "Barclay",
          address: "795-6380 Augue Street",
          phoneNumber: "16230129 6915",
          alternateNumber: "06302614899",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "12/30/93"
        },
        {
          name: "Bree",
          address: "P.O. Box 145, 4422 Feugiat Road",
          phoneNumber: "16401114 2322",
          alternateNumber: "84360380599",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "07/07/74"
        },
        {
          name: "Hop",
          address: "Ap #294-2280 Integer Rd.",
          phoneNumber: "16211114 9536",
          alternateNumber: "62614795999",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "03/12/93"
        },
        {
          name: "Lyle",
          address: "P.O. Box 275, 9744 Est Street",
          phoneNumber: "16490927 5325",
          alternateNumber: "21881069499",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "04/12/45"
        },
        {
          name: "Ulla",
          address: "625-342 Natoque Av.",
          phoneNumber: "16120103 6140",
          alternateNumber: "75781683699",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "10/03/92"
        },
        {
          name: "Barry",
          address: "423-4954 Suspendisse Street",
          phoneNumber: "16580612 8400",
          alternateNumber: "33810425099",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "11/28/53"
        },
        {
          name: "Chancellor",
          address: "359-6400 Dictum Av.",
          phoneNumber: "16640921 6881",
          alternateNumber: "68281866499",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "08/07/58"
        },
        {
          name: "Blythe",
          address: "4149 Nec Street",
          phoneNumber: "16890721 7676",
          alternateNumber: "06392981399",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "11/13/53"
        },
        {
          name: "Maggie",
          address: "521-9609 Mi Ave",
          phoneNumber: "16351108 6344",
          alternateNumber: "35969681199",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "04/11/78"
        },
        {
          name: "Martin",
          address: "4471 Condimentum Avenue",
          phoneNumber: "16540122 0545",
          alternateNumber: "93517245599",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "11/13/85"
        },
        {
          name: "Seth",
          address: "Ap #912-7541 Lacinia Ave",
          phoneNumber: "16300406 3867",
          alternateNumber: "20272478299",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "01/24/59"
        },
        {
          name: "Colette",
          address: "P.O. Box 614, 8779 Urna. Ave",
          phoneNumber: "16310523 1694",
          alternateNumber: "49592998399",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "10/04/26"
        },
        {
          name: "Winter",
          address: "8740 Morbi Street",
          phoneNumber: "16600213 3335",
          alternateNumber: "47220650799",
          image: 'https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg',
          status: 'Available',
          dob: "10/02/26"
        }
      ]
    };
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
