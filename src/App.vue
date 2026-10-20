<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Product from './components/Product.vue'
import Contact from './components/Contact.vue'
import Mybooking from './components/Mybooking.vue'
import Modal from './components/Modal.vue'
import Footer from './components/Footer.vue'



export default {
  components: {
    Navbar,
    Home,
    About,
    Product,
    Contact,
    Mybooking,
    Modal,
    Footer,

  },
  data() {
    return {
      currentPage: 'Home',
      modalPage: false,
      service: [],
      toBooking: [],
    }
  },
  methods: {
    setPage(page) {
      this.currentPage = page;
    },

    openModal(i) {
      this.service.push(i);
      this.modalPage = true;
    },

    closemodal(a) {
      this.modalPage = a;
    },

    receivedProduct(index) {
      this.service.push(index)
    },
    sendToBooked(name){
      this.toBooking.push(name)
      console.log(this.toBooking)
    }

  },
}
</script>



<template>

  <Navbar @goTo="setPage" />
  <Home v-if="currentPage === 'Home'" />
  <About v-if="currentPage === 'About'" />
  <Product v-if="currentPage === 'Product'" @send-services="openModal" />
  <Contact v-if="currentPage === 'Contact'" />
  <Mybooking v-if="currentPage === 'Mybookingl'" :booking="service" :mao="toBooking" />

  <Modal v-if="modalPage" @close="closemodal" :serviceName="service" @send-item="sendToBooked"/>
  <Footer />

</template>
