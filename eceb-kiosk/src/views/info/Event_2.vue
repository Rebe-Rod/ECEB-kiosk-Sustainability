<template>
  <div class="why-care page">
    <div class="info-title">
      Energy Efficiency Day
    </div>

    <div id="blur-card">

    <ul id="why-care-data-list">
      <li v-for="data in eventData2" :key="data.title + '-list-item'" class="data-list-item">        
        <div class="data-title">
          {{data.title}}:
        </div>
        <div class="data-description">
          {{data.description}}
        </div>
      </li>
      <li class="data-list-item qr">
        <div class="data-title">
          Learn More By Scanning The QR Code Below!
        </div>
        <v-img class ="event-image" src="../../assets/EnergyEfficiencyDay_QRCode.png"/>
      </li>
    </ul>

    </div>


    <div class="footer">
      <Footer></Footer>
    </div>
    
    
  </div>
</template>

<script>
import Footer from "../../components/Footer.vue"
import {eventData2} from "../../const"
export default {
  name: 'WhyCare',
  data: () => ({
    eventData2: eventData2
    }),
  methods: {

  },
  components : {
   Footer
 },
}
</script>

<style scoped>

  .info-title {
    position: absolute;
    width: 100%;
    height: 100%;
    background: linear-gradient(-45deg, rgba(232,74,39,1) 0%, rgba(19,41,75,1) 75%);
    background-size: 250% 100%;
    animation: gradient 30s ease infinite;
    margin: 0;
    padding: 0;

    font-family: ProximaNovaBold;
    font-size: 54px;
    color: white;
    padding: 37px 75px;
    line-height: 48px;
  }

  #blur-card {
    position: absolute;
    background-color: rgb(179, 179, 179, 0.2);
    left: 125px;
    top: 130px;
    width: auto;
    height: auto;
    padding: 20px 40px;
    

    border-radius: 40px;
  }

  #why-care-data-list {
    position: relative;
    width: 1605px !important;
    width: auto;
    height: auto;
    list-style: none;
    color: white;
    font-size: 32px;
  }

  .data-list-item {
    margin-bottom: 20px;
    background-color: rgba(0,0,40,0.5);
    border-radius: 25px;
    padding: 15px;
    width: 1200px;
    height: 785px;
  }

  .data-title {
    font-weight: bold;
    font-size: 40px;
    color: #7eaffc;
    line-height: 100%;
    padding-bottom: 5px;
    padding-left: 20px;

  }

  .data-description {
    padding-right: 25px;
    white-space: pre-line;
    padding: 20px;

  }

  .event-image {
    width: 285px;
    height: 285px;
    left: 35px;
    border-radius: 40px;
    top: 105px;
  }

  ul {
    padding-left: 0;

  }

  ul li {

        float: left;
  }

  .qr {
    margin-left: 20px;
    width: 385px;
  }

</style>