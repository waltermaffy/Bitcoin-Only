<template>
  <transition name="modal-fade">
   
 
    <div class="modal-overlay" @click="$emit('close-modal')">
      <div class="modal" @click.stop>
      </div>

      <div class="close" @click="$emit('close-modal')">
        <div class="quote-wrapper">
          <div class="inner">
            <h3>Stai donando Sats a {{peer}}</h3>
            
            <h3>Lightning Address</h3>

              <!-- <p>{{donation.lnaddress}}</p>
              <a v-if="donation.lnaddress" >{{ donation.lnaddress }}</a>
						  <div v-else>No Lightning Address</div>
              <p>{{donation.lnaddress}}</p> -->
            
            <h4>LNURL</h4>
            
            <p6 class="lnurl-text">LNURL1DP68GURN8GHJ7MR9VAJKUEPWD3HXY6T5WVHXXMMD9AKXUATJD3CZ7CTSDYHHVVF0D3H82UNV9U6NGV3JEA3304</p6>
            <!-- <p6 class="lnurl-text">{{donation.lnurl}}</p6> -->
            <a id="cryptodonate-wallet" target="_blank"
               href="" title="Click here to send this address to your wallet.">
              <img src="/icons/wallets.svg">
            </a>

            <p>QR code image</p>
            <!-- <qr-code text="Text to encode"></qr-code> -->
                 <!-- <QRCodeVue3
          value="Simple QR code"
        /> -->
            <button>Close</button>
          </div>
        </div>
        
      </div>
    </div>
  </transition>
</template>

<script>

// import QRCodeVue3 from "qrcode-vue3";
// import VueQRCodeComponent from 'vue-qrcode-component'
export default {

	// components: {  },

  props: [
    'peer', 'donation',
  ]
}
</script>

<style lang="scss" scoped>

@import 'assets/css/pages.scss';
@import 'assets/css/donate-component.scss';

.lnurl-text {
  
}
</style>