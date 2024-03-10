<template>
  <div class="container">
    <div>test</div>
    <button @click="connect">connect wallet</button>
    <div id="connect-wallet"></div>
  </div>
</template>

<script>
  import WebApp from '@twa-dev/sdk'
  import TonConnect from '@tonconnect/sdk';
  import { TonConnectUI } from '@tonconnect/ui'

  export default {
    name: 'IndexPage',
    data() {
      return {
        connector: null,
      };
    },
    async mounted() {
      this.connector = new TonConnectUI({
        manifestUrl: 'https://likecataa.github.io/test-ton-mini/tonconnect-manifest.json',
        buttonRootId: 'connect-wallet'
      }); 

      WebApp.ready();

      
    },
    methods: {
      async connect() {

      },
    }
  }
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .title {
    font-family:
      'Quicksand',
      'Source Sans Pro',
      -apple-system,
      BlinkMacSystemFont,
      'Segoe UI',
      Roboto,
      'Helvetica Neue',
      Arial,
      sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .links {
    padding-top: 15px;
  }
</style>